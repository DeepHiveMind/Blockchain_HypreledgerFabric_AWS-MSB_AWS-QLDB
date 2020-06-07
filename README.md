# Blockchain Hyperledger-Fabric AWS-QLDB AWS-MSB
 A quick Rundown
- [Blcokchain Quick Overview](#Blcokchain-Quick-Overview)
	
	- [A Sneak Peek into widely used Blockchain frameworks](#A-Sneak-Peek-into-widely-used-Blockchain-frameworks)
	- [Multiple Blcokchain Frameworks](#Multiple-Blcokchain-Frameworks)
	- [When to use Which Framework](#When-to-use-Which-Framework)

- [(1) Hyperledger Fabric HLF](#Hyperledger-Fabric-HLF)
	- [Overview of Hyperledger Framework & Tools](#Overview-of-Hyperledger-Framework-and-Tools)
	- [Key Concpets of HLF](#Key-Concpets-of-HLF)
	
- [(2) AWS Quantum Ledger Database QLDB](#AWS-Quantum-Ledger-Database-QLDB)
	- [Overview of AWS QLBD](#Overview-of-AWS-QLBD)
	- [Use Cases application of QLDB for Data ENGINEERS & DATA ARCHITECTS](#Use-Cases-application-of-QLDB-for-DATA-ENGINEERS-and-DATA-ARCHITECTS)
	- [Implementation Architecture Solution using QLDB](#Implementation-Architecture-Solution-using-QLDB)
	
- [(3) AWS Managed Blcokchain AMB](#AWS-Managed-Blcokchain-AMB)


This repo primarily intends to canvass for 3 following major framework/services for Blcokchain
- **Hyperledger-Fabric** 
- **AWS-QLDB (AWS Quantum Ledger Database)**
- **AWS-MSB (AWS Managed Blockchain)**
Real world application of one of above Blockhain service 
	- **Use Cases application of Blockchain Network for ENTERPRISE DATA LAKE ENGINEERING and for DATA ARCHITECTS**
	- Digital Asset Management


*For the ease of addressing, hereon, I'll use following pairs of terms interchangably* - 
- Hyperledger-Fabric as **HLF**
- Hyperledger as **HL**
- AWS-QLDB as **QLDB**
- AWS MSB as **MSB**
 
***
This repo primarily intends to offer distillation of my experience in 3 major Blcokchain frameworks - HLF, QLDB & MSB. 
Please note: 
 - There are very many other popular Blockchain frameworks and tools available in the market in addition to the chosen ones in this repo, such as 
		- 
 
 - Many of these aforemention Blcokchain framework/services are very popular, and are being extensively used.
 - This repo doesn't intend to draw any sort of comparative view between the chosen framework/services and other popular frameworks.
 - This is truly illustrative in nature. 

***


# Blcokchain Quick Overview 

### Multiple Blcokchain Frameworks

Just a sneak peek into Blcokchain Frameworks through Infographics:

|Blcokchain Framework Conceptual difference | Broader View of Blcokchain Framework|  Commonly used Blcokchain Framework|
| :--: | :--: | :--: |
|<img src="/img/conceptualBC.png" width="300" Height="250" />|<img src="/img/broaderBC.png" width="300" Height="250" />|<img src="/img/commonBC.png" width="300" Height="250" />|
|Click on above image for full view|Click on above image for full view|Click on above image for full view|

### A Sneak Peek into the FEATURES of widely used Blockchain frameworks

Sneak Peek into the FEATURES of various commonly known Blockchain frameworks: 


Blcokchain Frameworks do vary based on distinct needs, i.e., please choose the right framework from very many Blockchain framework options based on whether you need 
- a **Centralized ledger** database {such as Etherum (Public)/ AWS QLDB (Private)},
- or a **Multi-party** {Channel Management for multiple stakeholder Scenario - such as Hyperledger Fabric}, 
- or a **Fully managed blockchain network** that helps eliminate intermediaries {such as, AWS Managed Blockchian on HLF}
	
However, The commonality amongst All of the types of available frameworks
- **DAPP**: Blcokchain is a DAPPs (Decentralized Applications). 
- **Data Provenance**: Blcokchain comes baked in with *Data Provenance* by offering *immutable and cryptographically verifiable record of transactions* 
- each offers an **immutable** and **cryptographically verifiable record of transactions** 
- each one is also available in **DOCKER (containers)**
- Full Scale Operationalization Paradigm: **BlcokchainOps**: *DevOps in Blockchain*-  One can use **Kubernetes (CaaS)** to seamlessly manage and govern these Blockchain containerized network, workloads (smart contracts, Member registry et al) with the High availability, Auto Scalability, Self healing NFRs. 

 
SOR vs Blcokchain from **Business Network** standpoint:




### When to use Which Framework

Q. A Specific Question, per say : *"When to use Hyperledger Fabric & When to use Etherum?"*

A. Hyperledger Fabric is well-suited for applications that require *stringent privacy and permission controls with a known set of members*.
     - for example, a ```financial application``` where certain ```trade-related data is only shared with select banks``` .
	 - Ethereum can also be used for joining a public Ethereum blockchain network.
	 
   Whereas, Ethereum is well-suited for highly distributed blockchain networks where transparency of data for all members is important, 
	 - for example, a ```customer loyalty``` blockchain network that allows ```any retailer in the network to independently verify a user's activity across all members to redeem benefits```. 
	 
### Blockchain for DATA TRUST in ENTERPRISE DATA LAKE ENGINEERING world

Businesses & Regulatory compliance (e.g., GDPR) often need a system-of-record application with 
 - **(a) Auditing capability** to keep track of critical data, 
 - **(b) establish Data provenance**, 
 - **(c) Verifiability** 
 in order to evolve it to the maturity of **TRUSTED SOR or Systems-of-engagement (DWH/ Data lake)**.
				
We all know, *building TRUST (audit functionality & Verifiability)* with **Next Gen Distributed Relational databases/NOSQL Distributed Databases** 
- requires **custom development**,
- is **time-consuming**,
- prone to human error,
- as in case of relational databases/ NOSQL DBs are not inherently *immutable*, any **unintended changes** to the data are hard to track and verify. **verifiability** is tougher implementation ask.

*BLOCKCHAIN NETWORK IS THE SILVER BULLET FOR SUCH SCENARIO IN DATA ENGINEERING AND DATA LAKE TRUST.*.

**"Blcokchain" vis-a-vis "Today’s Systems-of-Record"**: 
{A VERY IMP PERSPECTIVE for **ENTERPRISE DATA PROCESSING & DATA LAKE ARCHITECTS**}
   ```	
"Today’s Systems-of-Record" is a
	- *'Distributed Database/ Ledger Management system'* 
	- wherein all the members of a **business network** transact with each other, 
	- but they maintain **separate records of their transactions**.
				
				- 
		
		- "Blcokchain" is the Future network which answers aforemention inherent challanges with traditional SOR 
				- with *'Distributed' & 'Decentralized' Database/ Ledger Management system* 
				- wherein auditing, record keeping and **Data provenance** comes baked in 
```
	
	

|"Today’s Systems-of-Record" (Distributed Database or Ledger) | "Blcokchain" (The Future network of Distributed and Decentralized Database or Ledger)|
| :--: | :--: |
|<img src="/img/current_fin_network_SOR.png" width="300" Height="250" />|<img src="/img/future_net_BLOCHAIN.png" width="300" Height="250" />|
|Click on above image for full view|Click on above image for full view|
|**private programs** & **private Ledger** for Every participant | **shared programs** and **shared ledgers** for Every participant|


# Hyperledger Fabric HLF
- The Linux Foundation founded the Hyperledger project in Y2015 to advance cross-industry blockchain technologies. 
- HLF is one of the Framework from *"HL Framework & Tools ecosystem"* with the primary objective to provide **Permissioned with Channel Support**. i.e., HLF is one of the blockchain projects within Hyperledger.

- Like other blockchain technologies (Etherum), it also has 
		- a ledger, 
		- uses smart contracts, 
		- participants manage their transactions,
		- Data Provenance* by offering *immutable and cryptographically verifiable record of transactions* 
		
- Unlike other Blockchain technologies (Ethereum), it differs as
		- private and permissioned,
		- No open permissionless system,
		- No unpermissioned entry to any member/*unknown identities* to participate in the network,
		- No PoW ( “proof of work” protocol to validate transactions and secure the network),
		- Membership Service Provider (MSP):  Restricted Entry to Members of a Hyperledger Fabric network enroll through a trusted MSP

### Overview of Hyperledger Framework and Tools 

Broader ecosystem of *HL Framework & Tools:*

<img src="/img/HLBroaderView.png" width="800" Height="300" />

[Source](https://www.hyperledger.org/wp-content/uploads/2018/07/HL_Whitepaper_IntroductiontoHyperledger.pdf)

### Key Concpets of HLF

- Blockchain network:
	A blockchain network is a technical infrastructure that provides ledger and smart contract (chaincode) services to applications

- Block & Chain: 
	A block contains an ordered set of transactions. It is cryptographically linked to the preceding block, and in turn it is linked to be subsequent blocks.

	The ledger’s chain is a transaction log structured as hash-linked blocks of transactions. Suuch as, Blockchain B contains blocks 0, 1, 2.
	
- Smart Contract:

	A smart contract is code (invoked by a client application external to the blockchain network) that manages access and modifications to a set of *key-value pairs* in the *World State* via Transaction.

	
- Chain Code:

	In Hyperledger Fabric, smart contracts are packaged as chaincode. Chaincode is installed on peers and then defined and used on one or more channels.

- World State:

	*World state* maintains  “current state” of transaction in Ledger, and such data is stored in a state database for efficient reads and queries from chaincode. Supported databases include - *couchDB*.
	
- Channel:
	
	A channel is a private blockchain *overlay* which allows for data isolation and confidentiality. A channel-specific ledger is shared across the peers in the channel, and transacting parties must be authenticated to a channel in order to interact with it. Channels are defined by a *Configuration-Block*.
	
- Membership Service Provider:

	MSP refers to an abstract component of the system that provides credentials to clients, and peers for them to participate in HLF.

- Ordering Service:

	Also known as orderer. A defined collective of nodes that orders transactions into a block and then distributes blocks to connected peers for validation and commit. The ordering service exists independent of the peer processes and orders transactions on a first-come-first-serve basis for all channels on the network.


***
HLF also leverages *Gossip Protocol* & *Raft Algo* for following 3 major functions:
	- 1) manages peer discovery and channel membership; 
	- 2) disseminates ledger data across all peers on the channel; 
	- 3) syncs ledger state across all peers on the channel

The same *protocol* and *Algo* is used in **Progrium Consul** (a distributed computing CONSENSUS Algo for Leader election and worker management), and it is applied in Seneca (a Microservice Framework on Nodejs)
***






# AWS Quantum Ledger Database QLDB

### Overview of AWS QLBD
AWS QLDB
- is **Scalable**
- is **Serverless**
- provides a **centralized ledger** for auditing and record keeping purposes
- Offers **Verifiability** - verifies integrity of past records 
- can be provisoned with **AWS ClouFormation (IaC)** with additional user level control from clinet side with **IAM & ACL**
- can **trigger AWS Lambda events** to process other *downstream workflows* 
- can integrate with **other AWS PaaS Services**
	
### Use Cases application of QLDB for DATA ENGINEERS and DATA ARCHITECTS	

*Use Case:*

Businesses, Regulatory compliance (e.g., GDPR) often need a Data Lake / Data Foundation / System-of-Engagmemt to have Comprehensive Data Trust pillars (audit, provenance, Lineage, Verifiability). But, the Organization (a large FinTech Org) wants to have Furute-gen architecture which can provide

- enablement of the Comprehensive Data Trust pillars (audit, provenance, Lineage, Verifiability)**@port-of-entry** of System-of-Engagmemt
  ```
	- auditing capability to keep track of critical data 
	- Data Provenance 
	- complete history of assets / Data Lineage
	- Verifiability : a verification mechanism to verify integrity of past records
  ```
- Post enablement of DATA TRUST pillars @port-of-entry, it should be able to trigger serverless-processing or serverless-workflows for 
  ```
	- caching the history for querying in Amazon Elasticsearch, 
	- transforming and loading the data into an Amazon Redshift cluster, and 
	- also storing the data in an Amazon S3 data lake.
   ```
- for critical events originating from **Streaming sources**, such as "*credit* and *debit transactions* across bank accounts", and also
- for critical datasets generating from **Batch sources**, such as "history of assets for Loan lending to Orgs/customers like vehicle maintenance records /or/ Lending application records".


### Solution Architecture Solution using QLDB

Architecture Solution using QLDB for above use case application:

<img src="/img/Architecture_QLDB_non-traditionalSOR.png" width="900" Height="500" />

	


# AWS Managed Blcokchain AMB

### Key Concpets of AMB

# Reference
[1]

[2]https://github.com/senlinuc/caffe_ocr
