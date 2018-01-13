VeraTrade Technical Design
==========================

Architecture
------------
Any organization that wants to operate a network can participate by running a VeraTrade compliant server. Note that each VeraTrade Server will be responsible for processing API calls, storing data in a local database, updating the public blockchain, triggering email notifications, and providing services for user interactions. Interop services allow a newly provisioned server to load past transactions based on one or more blockchain addresses.

The proposed solution requires three levels of data storage:

1. Blockchain - Used for immutable storage of commitments, status updates and transactions hashes for versioning.

2. Public blobs - Used to publish documents to supply chain partners

3. Relational database - Used for local operation of server application

The proposed solution requires support for six transaction types which are explained below:
1. Purchase Order
2. Purchase Order Acknowledgement
3. Purchase Order Status Update
4. Shipment
5. Shipment Acknowledgement
6. Shipment Status Update

### General API Guidelines
The proposed solution implements REST API end points for each transaction type as well as some support service endpoints. Each API endpoint will have a structure like:

{{url}}/api/{{version}}/purchaseOrder

*url* is the fully qualified domain name of the server and *version* is the specification version of this standard preceeded by a *v*. For example, a server hosted on https://veratrade.domain.com using version .1 of this specification would implement the following endpoint:

https://veratrade.domain.com/api/v.1/purchaseOrder

Each transaction type supports the following standard HTTP verbs:
- GET - Retrieves an existing transaction
- POST - Creates a new transaction 
- PUT - Edits an existing transaction
- DELETE - Cancels an existing transaction

Data payloads for transactions should be formatted using JSON and are described below.

### Purchase Order 

#### Overview
When the buyer is ready to place an order to a supplier, a Purchase Order transaction should be created on a VeraTrade Server. The server will send email notifications to the supplier and carrier based on the distribution list provided by the buyer. As with all transactions, Purchase Orders can be created through a web interface on the VeraTrade Server or through an API call.

#### User Interface
If the buyer chooses they can enter Purchase Orders manually on a web form provided by the VeraTrade Server. The user interface will support entry of Purchase Order header, parties, and line items. The server should offer master data management for parties and products to speed data entry on subsequent Purchase Orders.

#### API
A Purchase Order transaction can be posted directly to the VeraTrade server's Purchase Order Transaction endpoint. This makes it possible to build integrations between the buyer's ERP system and the VeraTrade Server.

The endpoint must follow the below structure:

{{url}}/api/{{version}}/purchaseOrder

The Purchase Order Transaction must be formatted using the below structure:

```
{
    "purchaseOrderNo" : "ORD10923",
    "purchaseOrderDate : "2018-01-15T09:45:00-08:00",
    "requestedShipDate" : "2018-02-07T17:00:00-08:00",
    "requestedDeliveryDate" : "2018-02-19T17:00:00-08:00",
    "buyer" : {
        "address" : "0xb65afc2aa59856a3e76f50d4ad43e596343b82ca",
        "name" : "JetPack Corporation",
        "address1" : "7600 Flight Avenue",
        "address2" : "",
        "city" : "Los Angeles",
        "state" : "CA",
        "postalCode : "90501",
        "countryCode" : "US",
        "telNo" : "13103832087",
        "distributionList" : [
            {
                "emailAddress" : "george@jetpack.com"
            },
            {
                "emailAddress" : "joe@jetpack.com"
            }
        ]               
    }    
    "supplier" : {
        "name" : "Hongtai Electronics",
        "address1" : "No. 2975 Hai An Zhen Feng",
        "address2" : "",
        "city" : "Shanghai",
        "state" : "Jiangsu Province",
        "postalCode : "22800",
        "countryCode" : "CN",
        "telNo" : "866103832087",
        "distributionList" : [
            {
                "emailAddress" : "sam@hongtai.com"
            },
            {
                "emailAddress" : "betty@hongtai.com"
            }
        ]       
    }        
    "shipTo" : {
        "name" : "JetPack Corporation",
        "address1" : "7600 Flight Avenue",
        "address2" : "",
        "city" : "Los Angeles",
        "state" : "CA",
        "postalCode : "90501",
        "countryCode" : "US",
        "telNo" : "13103832087"
    },
    "incoterms" : "EXW",
    "carrier" : {
        "name" : "Standard Shipping Line",
        "telNo" : "866103938218",
        "distributionList" : [
            {
                "emailAddress" : "alvin@standard.com"
            },
            {
                "emailAddress" : "joe@standard.com"
            }
        ],
        "accountNo" : "993882993"
    },
    "requestedUpdateFrequency" : {
        "timeUnit" : "Day",
        "timeValue" : 7
    },
    "items" : [
        {
            "lineNo" : "1",
            "buyerProductNo" : "T9928",
            "sellerProductNo" : "102998",
            "quantityOrdered" : 1500,
            "quantityUnit" : "EA",
            "unitPrice" : .73,
            "currencyCode" : "USD",
            "requestedShipDate" : "2018-02-07T17:00:00-08:00",
            "requestedDeliveryDate" : "2018-02-19T17:00:00-08:00"
        },
        {
            "lineNo" : "2",
            "buyerProductNo" : "T93827",
            "sellerProductNo" : "102265",
            "quantityOrdered" : 700,
            "quantityUnit" : "EA",
            "unitPrice" : 1.25,
            "currencyCode" : "USD",
            "requestedShipDate" : "2018-02-07T17:00:00-08:00",
            "requestedDeliveryDate" : "2018-02-19T17:00:00-08:00"
        }        
    ]
}

```

#### Workflow 
When a Purchase Order is created on a VeraTrade Server (either through the user interface or the API), the following workflow will execute:

1. The Purchase Order will be saved in the VeraTrade Server's local database. 
2. A SHA256 hash will be generated from the JSON Purchase Order Transaction. A new Purchase Order entry will be added to the VeraTrade smart contract that includes the Purchase Order hash, the VeraTrade Server's fully qualified domain name, and the buyer's address.
3. A notification will be sent to the supplier email addresses listed in the Purchase Order transaction. The email body will display Purchase Order details. A *magic link* will be included in the email which will allow the supplier to authenticate against the VeraTrade server, view the Purchase Order details, and proceed with the Purchase Order Acknowledgement when ready.
4. If the supplier does not acknowledge the Purchase Order within 24 hours of creation, a reminder notification will be generated. Two additional reminders will be sent over 24 hour periods. If the supplier has not acknowledged the purchase order 24 hours after the last reminder, a notification will be sent to the buyer email addresses listed in the Purchase Order transaction stating that the supplier has not acknowledged the purchase order.

### Purchase Order Acknowledgement
#### Overview
#### User Interface
#### API 
#### Workflow 
When a Purchase Order is acknowledged by the supplier, the following workflow will execute:

1. The Purchase Order Acknowledgement will be saved in the VeraTrade Server's local database.
2. The Acknowledgement status, projected ship date, and timestamp will be added to the Purchase Order's entry on the smart contract.
3. A notification will be set to the buyer email addresses listed in the original Purchase Order transaction. The email body will provide details about the Purchase Order Acknowledgement. A *magic link* will be included in the email that allows the buyer to authenticate against the VeraTrade Server and view the Purchase Order Acknowledgement Details.
4. If a carrier was provided in the original Purchase Order Transaction, a notification will be sent to the carrier email addresses listed in the original Purchase Order transaction. The email body will provide basic information about the Purchase Order along with the projected ship date. A *magic link* will be included in the email which will allow the carrier to authenticate against the VeraTrade Server and work with the Purchase Order.

### Purchase Order Status Update
#### Overview
#### User Interface
#### API 
#### Workflow 

### Shipment 
#### Overview
#### User Interface
#### API 
#### Workflow 

### Shipment Acknowledgement
#### Overview
#### User Interface
#### API 
#### Workflow 

### Shipment Status Update
#### Overview
#### User Interface
#### API 
#### Workflow 

### Support Services 
#### Overview
#### User Interface
#### API 
#### Workflow 