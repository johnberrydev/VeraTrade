VeraTrade Whitepaper
==============================
### Supply Chain Transparency Using Open Source Blockchain Technology

Abstract
--------
This whitepaper proposes to create an open source supply chain operating network backed by blockchain technology. This solution will help buyers optimize their supply chain processes and deliver transparency across suppliers and carriers.

Problem
--------
International supply chains have always suffered from a lack of transparency which creates billions of dollars of waste for the global economy each year. In a business-to-business purchase there are three general parties involved:

- Buyer - The organization purchasing goods necessary for their business.
- Supplier - The manufacturer or distributor of the goods which will ship to buyer
- Carrier - The transportation provider that handles the shipment from the supplier to the buyer. This may be a common carrier, a non-asset based logistics provider, or a combination of the two.

These three parties and various other participants collaborate to fulfill the buyer's order. Usually these three parties are unrelated companies each with their own interests. This leads to restricted information exchange between the parties. Although transactions are completely dependent on the buyer, it is often difficult for buyers to obtain accurate status about their orders. There are two primary reasons for this lack of transparency:

- Boundaries - There are many types of boundaries that separate these parties and inhibit the flow of information. There are organizational boundaries, geographic boundaries, cultural boundaries, and technology boundaries. A simple example is time zone differences. If a buyer in the United States needs information from their supplier in China, they may have to wait several hours until the supplier's business day starts.

- Misaligned Incentives - Supply chains suffer from a classic *principal-agent problem*. This describes scenarios where a person or organization (the agent) can make decisions that impact another person or organization (the principal), yet the agent is motivated by their own self-interest rather than those of the principal. In an international supply chain the supplier and carrier cannot exist without the buyer. However they are primarily concerned with their own profits. This results in a misalignment of incentives from the buyer's perspective. Although the buyer needs full transparency into order status, suppliers and carriers benefit from ambiguity. When things go wrong, the supplier and carrier avoid exposing their responsibility in the failure. When a buyer holds a supplier accountable for service failures, it is costly for the supplier to respond and it threatens their future business. 

Boundaries make transparency inefficient and expensive. Misaligned incentives put transparency in opposition to the financial interests of supply chain participants. The result is that buyers have limited visibility about order status. This lack of transparency at a transactional level creates many economic problems for the buyer:

1. Higher inventory costs - In the absence of reliable status about incoming purchase orders, the buyer must maintain a large buffer of inventory to fulfill outgoing sales orders. Inventory ties up a company's financial resources. Inventory is risky since it can expire or become obsolete prior to sale. 

2. Increased labor costs - Without a trusted source for visibility information, the buyer must constantly follow up on orders to determine if there is a problem. This is extremely labor intensive and requires a special skill set to overcome the boundaries that prevent flow of information. Despite advancements in cloud, internet of things, and modern data integration practices, most buyers manage their supply chains with manual email communications. 

3. Increased fulfillment costs - Buyers ultimately sell their products through various sales channels like distributors, retail, and eCommerce. These channels frequently enforce various fees and penalties to ensure fulfillment service levels are met. For example, Walmart and Amazon often charge penalties when product is not delivered by the required date. Without reliable upstream visibility, these costs become much more frequent. 

4. Decreased agility - The ability to adapt to market changes is a key competitive advantage in today's fast-moving economy. Without supply chain transparency, buyers cannot proactively respond to changes. Whether it's a sudden increase in demand or a supply chain disruption, the buyers that respond quickly are the ones that will ultimately survive. 

Lack of verifiable performance data
----------------------------------
Without transparency there is no trustable record of past performance to support buyers' decision making. When buyers source new suppliers or carriers, it is quite common for performance metrics to be completely fabricated. Suppliers will state that they meet manufacturing deadlines 99% of the time. Carriers state they meet delivery deadlines 99% of the time. There is no way for buyers to validate these metrics. The reality is that the suppliers and carriers often don't have the ability to measure performance at all due to immature processes or systems. Without any reliable performance data, it is nearly impossible for buyers to make empirical decisions about which suppliers and carriers to work with.

A key responsibility for supply chain professionals is to make the best possible decisions in a world with a high level of uncertainty. Over the years many strategies have been applied to supply chain optimization including lean, on-shoring, point-to-point EDI, and SaaS order management tools. However there is no magic solution and each strategy has its own set of compromises. To date there is no pervasive approach that has demonstrated reliable results in solving the problem of supply chain transparency. 

Solution
--------
The proposed solution to the transparency problem is an open source *supply chain operating network* backed by *blockchain* technology. The supply chain operating network consists of an application that manages order flow between the buyer, supplier and carrier. It also provides data integration hooks that allow each participant to integrate their own systems into the network. When buyers, suppliers and carriers choose to collaborate on a single operating network, many of the boundary problems can be overcome. 

A key element of the solution is that the supply chain operating network will be *open source* and *decentralized*. This approach offers flexibility, reduced implementation costs, and will support pervasive growth of the network. The solution consists of a standard set of interface protocols along with a fully functional reference implementation which will be open source. Supply chains can immediately start transacting commerce on the reference implementation, or they can build their own software that complies with the standard interface protocols. 

The blockchain element of the solution provides two key benefits: 

1. A blockchain-based ledger provides an unchangeable record of transactions related to a purchase order. This creates a trusted source of truth across the buyer, supplier and carrier for each order. It also establishes a verifiable track record of past performance. Suppliers and carriers can now prove past performance results to current and potential customers. Blockchain eliminates the need for a central authority that manages the operating network and adjudicates disputes. It also eliminates the possibility that the operator of the network can unfairly influence performance results.

2. Smart contracts, a feature of some blockchains, can be used to align incentives more appropriately. Buyers will have the option to offer financial incentives in return for buyers and suppliers providing accurately and timely status updates about orders. Supply chain participants will collaborate on predicting outcomes as accurately as possible. A prediction market feature could also allow 3rd party experts or even AI algorithms to participate on outcome predictions. Although buyers will need to stake some financial resources for each transaction, they will receive quantifiable returns from savings on reduced inventories, reduce labor costs, increased agility, etc. 

### Key Functional Features
- Buyer order entry 
- Supplier order acceptance or rejection
- Supplier commitment on ship dates
- Supplier prediction on ship dates
- Supplier booking with carrier
- Carrier booking acceptance or rejection
- Carrier commitment on delivery date 
- Carrier prediction on delivery date
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

VeraTrade Foundation
--------------------
A non-profit organization will be established to manage the VeraTrade open source project. This organization will provide the following functions:

1. Management and documentation of API standards
2. Development and maintenance of the VeraTrade reference implementation
3. Hosting and infrastructure management for the VeraTrade reference implementation 


Competitors
-----------
Supply chain operating networks are not a new concept. Existing providers include Elemica, GTNexus, E2Open, and MP Objects. These providers have historically targeted larger enterprise customers whose transaction volume justifies return on investment. Another common model is when 3rd party logistics providers offer similar types of services to their customers either as paid service or a value-add to logistics services. 

All of these offerings are typically offered as a hosted web application combined with professional services to support implementation and data integration. These types of providers suffer from the following problems:

1. Cost - Since these provider's business models focus on the enterprise customer, their pricing is out of reach for most small to medium sized companies. These solutions are highly dependent upon establishing data integration with all supply chain participants. This adds significant costs to the project since both the supply chain participant and the operating network need to develop interfaces. Typically the buyer bears the data integration costs as part of the overall solution. 

2. Closed Systems - The value of these providers is limited by the size of their network. As more buyers and suppliers join a specific network the provider's value proposition improves for future customers that may already be trading with one of those companies. This creates a highly competitive zero-sum game between the leading networks. They focus on growing sales rather than interoperating with competing networks. This means an entire supply chain needs to agree on using a specific provider in order to achieve full value.

3. Central Authority – These networks are businesses that are primarily interested in their own profits. This can create conflicts of interest. Decisions about data usage, new features, or implementation priorities are controlled by the network and made in a way to optimize their financial gain. Even when a network has established a track record of trust, the situation can change dramatically when mergers and acquisitions occur.

4. Misaligned Incentives – The operating networks do not address the misaligned incentive problem. 

Roadmap
--------
Phase 1: Reference Implementation  
Phase 2: Server Interop  
Phase 3: Token-based Incentives  

Technical Design
-----------------
For information about the VeraTrade APIs and reference implementation see the [Technical Design](https://github.com/jtberry21/VeraTrade/blob/master/VeraTradeTechnicalDesign.md) 
