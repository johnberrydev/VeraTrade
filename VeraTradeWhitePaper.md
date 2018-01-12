VeraTrade Whitepaper
==============================
### Supply Chain Transparency With Open Source Blockchain Technology

Abstract
--------

Problem
--------
International supply chains have always suffered from a lack of transparency which create billions of dollars of waste for the global economy each year. In a business-to-business purchase there are three general parties involved:

- Buyer - The organization purchasing goods necessary for their business.
- Supplier - The manufacturer or distributor of the goods which will ship to buyer
- Carrier - The transportation provider that handles the shipment from the supplier to the buyer. This may be a common carrier, a non-asset based logistics provider, or a combination of the tow.

These three parties and various other participants collaborate to fulfill the buyer's order. Usually these three parties are unrelated companies each with their own interests. This leads to restricted information exchange between the parties. Although transactions are completely dependent on the buyer, it is often difficult for buyers to obtain accurate status about their orders. There are two primary reasons for this lack of transparency:

- Boundaries - There are many types of boundaries that separate these parties and inhibit the flow of information. There are organizational boundaries, geographic boundaries, cultural boundaries, and technology boundaries. A simple example is timezone differences. If a buyer in the United States needs information from their supplier in China, they may have to wait several hours until the supplier's business day starts.

- Misaligned Incentives - Supply chains suffer from a classic *principal-agent problem*. This describes scenarios where a person or organization (the agent) can make decisions that impact another person or organization (the principal), yet the agent is motivated their own self-interest rather than those of the principal. In an international supply chain the supplier and carrier cannot exist without the buyer. However they are primarily concerned with their own profits. This results in a misalignment of incentives from the buyer's perspective. Although the buyer needs full transparency into order status, suppliers and carriers benefit from ambiguity. When things go wrong, the supplier and carrier avoid exposing their responsibility in the failure. When a buyer holds a supplier accountable for service failures, it is costly for the supplier to respond and it threatens their future business. 

Boundaries make transparency inefficient and expensive. Misaligned incentives put transparency in opposition to the financial interests of supply chain participants. The result is that buyers have limited visibility about order status. This lack of transparency at a transactional level creates many economic problems for the buyer:

1. Higher inventory costs - In the absence of reliable status about incoming purchase orders, the buyer must maintain a large buffer of inventory to fulfill outgoing sales orders. Inventory ties up a company's financial resources. Inventory is risky since it can expire or become obsolete prior to sale. 

2. Increased labor costs - Without a trusted source for visibility information, the buyer must constantly follow up on orders to determine if there is a problem. This is extremely labor intensive and requires a special skill set to overcome the boundaries that prevent flow of information. Despite advancements in cloud, internet of things, and modern data integration practices, most buyers manage their supply chains with manual email communications. 

3. Increased fulfillment costs - Buyers ultimately sell their products through various sales channels like distributors, retail, and eCommerce. These channels frequently enforce various fees and penalties to ensure fulfillment service levels are met. For example, Walmart and Amazon often charge penalties when product is not delivered by the required date. Without reliable upstream visibility, these costs become much more frequent. 

4. Decreased agility - The ability to adapt to market changes is a key competitive advantage in today's fast moving economy. Without supply chain transparency, buyers cannot proactively respond to changes. Whether it's a sudden increase in demand or a large scale supply chain disruption, the buyers that respond quickly are the ones that will ultimately survive. 

Lack of verifiable performance data
----------------------------------
Without transparency there is no trustable record of past performance to support buyers' decision making. When buyers source new suppliers or carriers, it's quite common for performance metrics to be completely fabricated. Suppliers will state that they meet manufacturing deadlines 99% of the time. Carriers state they meet delivery deadlines 99% of the time. There is no way for buyers to validate these metrics. The reality is that the suppliers and carriers often don't have the ability to measure performance at all due to immature processes or systems. Without any reliable performance data, it is nearly impossible for buyers to make empirical decisions about which suppliers and carriers to work with.

A key responsibility for supply chain professionals is to make the best possible decisions in a world with a high level of uncertainty and ambiguity. Over the years many strategies have been applied including lean, on-shoring, point-to-point EDI, and SaaS order management tools. However there is no magic solution and each strategy has it's own set of compromises. To date there is no pervasive strategy that has demonstrated reliable results in solving the problem of supply chain transparency. 

Solution
--------
The proposed solution to the transparency problem is an open source *supply chain operating network* backed by *blockchain* technology. The supply chain operating network consists of an application that manages order flow between the buyer, supplier and carrier. It also provides data integration hooks that allow each participant to integrate their own systems into the network. When buyers, suppliers and carriers choose to collaborate on a single operating network, many of the boundary problems can be overcome. 

A key element of the solution is that the supply chain operating network will be *open source* and *decentralized*. This approach offers flexibility, reduced implementation costs, and will support pervasive growth of the network. The solution consists of a standard set of interface protocols along with a fully functional reference implementation. Supply chain participants can immediately start transacting commerce on the reference implementation, or they can build their own software that complies with the standard interface protocols. 

The blockchain element of the solution provides two key benefits: 

1. A blockchain-based ledger provides an immutable record of transactions related to a purchase order. This creates a trusted source of truth across the buyer, supplier and carrier for each order. It also establishes a verifiable track record of past performance. Suppliers and carriers can now prove past performance results to current and potential customers. Blockchain eliminates the need for a central authority that manages the operating network and adjudicates disputes. It also eliminates the possibility that the operator of the network can unfairly influence performance results.

2. Smart contracts, a feature of some blockchains, can be used to align incentives more appropriately. Buyers will have the option to offer financial incentives in return for buyers and suppliers providing accurately and timely status updates about orders. Supply chain participants will collaborate on predicting outcomes as accurately as possible. An prediction market feature could also allow 3rd party experts or even AI algorithms to participate on outcome predictions. Although buyers will need to stake some financial resources for each transaction, they will receive quantifiable returns from savings on reduced inventories, reduce labor costs, increased agility, etc. 

### Key Functional Features
- Buyer order entry 
- Supplier order acceptance or rejection
- Supplier commitment on ship dates
- Supplier prediction on ship dates
- Supplier booking with carrier
- Carrier booking acceptance or rejection
- Carrier commitment on delivery date 
- Carrier prediction on deliver date
- Buyer visibility from order to delivery
- Buyer reporting and analytics on supply chain performance

### Key Technical Features
- Published standards for transactional API and document schemas
- Support for distributed database storage (organizations or communities may choose to operate their own database)
- Pluggable integrations with ERP, TMS, and legacy EDI messages
- Email workflows
- Identity management and privacy controls
- Immutable record of past supply chain performance
- Token-based incentives
- Prediction market
- Oracle for determining truth of ship and delivery date

Process Walkthrough
-------------------

Competitors
-----------
Supply chain operating networks are not a new concept. Existing providers include Elemica, GTNexus, E2Open, and MP Objects. These providers have historically targeted larger enterprise customers whose transaction volume justifies return on investment. Another common model is when 3rd party logistics providers offer similar types of services to their customers either as paid service or a value-add to logistics services. 

All of these offerings are typically offered as a hosted web application combined with professional services to support implementation and data integration. These types of providers suffer from the following problems:

1. Cost - Since these provider's business models focus on the enterprise customer, their pricing is out of reach for most small to medium sized companies. These solutions are highly dependent upon establishing data integration with all supply chain participants. This adds significant costs to the project since both the supply chain participant and the operating network need to develop interfaces. Typically the buyer bears the data integration costs as part of the overall solution. 

2. Closed Systems - The value of these providers is limited by the size of their network. As more buyers and suppliers join a specific network the provider's value proposition improves for future customers that may already be trading with one of those companies. This creates a highly competitive zero-sum game between the leading networks. They focus on growing sales rather than interoperating with competing networks. This means an entire supply chain needs to agree on using a specific provider in order to achieve full value.

3. Central Authority -

4. Misaligned Incentives - 

Architecture
------------
Any organization that wants to operate a network can participate by running a VeraTrade compliant server. Note that Each VeraTrade Server will be responsible for processing API calls, storing data in a local database, updating the public blockchain, triggering email notifications, and providing services for user interactions. Interop services allow a newly provisioned server to load past transactions based on one or more blockchain addresses.

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


Roadmap
--------
Phase 1: Reference Implementation  
Phase 2: Server Interop  
Phase 3: Token-based Incentives  

Funding 
-------

