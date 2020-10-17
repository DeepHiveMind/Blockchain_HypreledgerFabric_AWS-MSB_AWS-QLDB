# Blockchain Hyperledger-Fabric AWS-QLDB AWS-MSB
 A quick Rundown of this Repo-
- [Blcokchain Quick Overview](#Blcokchain-Quick-Overview)
	- [Why Blockchain Matters More Than You Think](#Why-Blockchain-Matters-More-Than-You-Think)
	- [Multiple Blockchain Frameworks](#Multiple-Blockchain-Frameworks)
	- [A Sneak Peek into the FEATURES of widely used Blockchain frameworks](#A-Sneak-Peek-into-the-FEATURES-of-widely-used-Blockchain-frameworks)
	- [BlockchainOps- BLOCKCHAIN & DEVOPS](#BlockchainOPS)
	- [When to use Which Framework](#When-to-use-Which-Framework)
	- [Blockchain for DATA TRUST in ENTERPRISE DATA LAKE ENGINEERING world](#Blockchain-for-DATA-TRUST-in-ENTERPRISE-DATA-LAKE-ENGINEERING-world)
- [(Blockchain Tech # 1) Hyperledger Fabric HLF](#Hyperledger-Fabric-HLF)
	- [Overview of Hyperledger Framework & Tools](#Overview-of-Hyperledger-Framework-and-Tools)

	- [Hyperledger FABRIC, Hyperledger COMPOSER, Hyperledger EXPLORER](#Hyperledger-FABRIC-,-Hyperledger-COMPOSER-,-Hyperledger-EXPLORER)
	- [DOCKER Hyperledger FABRIC Hyperledger EXPLORER)(#DOCKER-Hyperledger-FABRIC-Hyperledger-EXPLORER)
	
- [(Blockchain Tech # 2) AWS Quantum Ledger Database QLDB](#AWS-Quantum-Ledger-Database-QLDB)
	- [Overview of AWS QLBD](#Overview-of-AWS-QLBD)
	- [PYTHON client API for AWS QLDB](#PYTHON-client-API-for-AWS-QLDB)
	
- [(Blockchain Tech # 3) AWS Managed Blcokchain AMB](#AWS-Managed-Blcokchain-AMB)

- [USE CASE IMPLEMENTATION](#USE-CASE-IMPLEMENTATION)
	- [(USE CASE #1) Application of Blockchain for DATA TRUST in ENTERPRISE DATA ENGINEERING](#Application-of-Blockchain-for-DATA-TRUST-in-ENTERPRISE-DATA-ENGINEERING)
		- [Solution Architecture using QLDB](#Solution-Architecture-using-QLDB)
	
	- [(USE CASE #2) Application of Blockchain for CIRCULAR SUPPLY CHAIN with IoT](#Application-of-Blockchain-for-CIRCULAR-SUPPLY-CHAIN-with-IoT)
		- [Solution ArchitectureHyperledgerFABRIC DOCKER AWS EKS IOT HSM](#Solution-Architecture-using-HyperledgerFABRIC-DOCKER-AWS-EKS-IOT-HSM)



***
This repo primarily intends to offer distillation of my experience in 3 major Blcokchain frameworks - HLF, QLDB & MSB. 
Please note: 
 - There are very many other popular Blockchain frameworks and tools available in the market in addition to the chosen ones in this repo. This repo primarily intends to canvass for 3 following major framework/services for Blcokchain
	- **Hyperledger-Fabric** 
	- **AWS-QLDB (AWS Quantum Ledger Database)**
	- **AWS-MSB (AWS Managed Blockchain)**
 
 - Many of these aforemention Blcokchain framework/services are very popular, and are being extensively used.
 - This repo is illustrative in nature. 


Following Real world application of one of above Blockhain service is exhibited in the repo
- **Application of Blockchain Network for ENTERPRISE DATA LAKE ENGINEERING and for DATA ARCHITECTS**
- **Digital Asset Management**
- **TRUSTED DATA PLATFORM** (System-Of-Enagements)
- **CIRCULAR SUPPLY CHAIN with IoT**


*For the ease of addressing, hereon, I'll use following pairs of terms interchangably* - 
- Hyperledger-Fabric as **HLF**
- Hyperledger as **HL**
- AWS-QLDB as **QLDB**
- AWS MSB as **MSB**
 

***


# Blcokchain Quick Overview 

Blockchain Technology is also addressed as 
	- **The Next Stage of Internet** 
	- **The Trustless system of Values** (wherein TRUST is injected by crptography, game theory and other technologies; rather than human being)
	- Technology quite *bigger and broader* than Bitcon
	
A Blockchain is 
- A *Transparent*, Cryptographically *Trusted* Dapp/dApp (Decentralized application) system used for **management & exchange** of *Digital assets* like Ownership title, Medical Datasets, CryptoCurrency without the need of any external human/other wise driven system for TRUST.
- A **cryptographic database** maintained by a network of computers, each of which **stores a copy of the most up-to-date version of Ledger**. It uses *Blockchain Protocol* for TRUST in *Transaction and Ledger management*.
- A **Blockchain protocol** is a set of rules that dictate how the computers in the network, called nodes, should 
	- *verify new transactions* and 
	- *add them to the database**. 
	
- The *Blockchain protocol* offers *Consensus building mechanism* by employing
 	- **Cryptography**, 
  	- **Game theory**, and 
  	- **Economics** 

to create incentives for the nodes to work
	- toward securing the network instead of attacking it for personal gain. 

- If the Blcokchain is set up correctly, this system can make it extremely difficult and expensive to add false transactions but relatively easy to verify valid ones.
- Blcokchain comes baked in with *Data Provenance* by offering 
	- immutable and 
	- cryptographically verifiable record of transactions

### Why Blockchain Matters More Than You Think


<table>
  <tr>
    <td width="20%">
        <a href="https://www.youtube.com/watch?v=GVN0Ddr3xig"> 6 MINS VIDEO </a> Explaining Why Blockchain Matters More Than You Think!
    </td>
    <td width="30%">
        <a href="https://www.youtube.com/watch?v=GVN0Ddr3xig"><img src="img/blockchain_vid1.JPG"></a>
    </td>
	    <td width="20%">
        <a href="https://www.youtube.com/watch?v=kP6EezXJKNM"> 16 MINS VIDEO </a> Explaining How Blockchain is Already Taking Over!
    </td>
    <td width="30%">
        <a href="https://www.youtube.com/watch?v=kP6EezXJKNM"><img src="img/blockchain_vid2.JPG"></a>
    </td>
  </tr>
</table>

### Multiple Blockchain Frameworks

Just a sneak peek into Blcokchain Frameworks through Infographics:

|Blcokchain Framework Conceptual difference | Broader View of Blcokchain Framework|  Commonly used Blcokchain Framework|
| :--: | :--: | :--: |
|<img src="/img/conceptualBC.png" width="300" Height="250" />|<img src="/img/broaderBC.png" width="300" Height="250" />|<img src="/img/commonBC.png" width="300" Height="250" />|
|Click on above image for full view|Click on above image for full view|Click on above image for full view|

### A Sneak Peek into the FEATURES of widely used Blockchain frameworks

Sneak Peek into the FEATURES of various commonly known Blockchain frameworks: 


Blcokchain Frameworks do vary based on distinct needs, i.e., please choose the right framework from very many Blockchain technology options based on whether you need 
- a **Centralized ledger** database {such as Etherum (Public)/ AWS QLDB (Private)},
- or a **Multi-party** {Channel Management for multiple stakeholder Scenario - such as Hyperledger Fabric}, 
- or a **Fully managed blockchain network** that helps eliminate intermediaries {such as, AWS Managed Blockchian on HLF}
	
However, The commonality amongst All of the types of available frameworks
- **DAPP**: Blcokchain is a DAPPs (Decentralized Applications). 
- **Data Provenance**: Blcokchain comes baked in with *Data Provenance* by offering *immutable and cryptographically verifiable record of transactions* 
- each offers an **immutable** and **cryptographically verifiable record of transactions** 
- each one is also available in **DOCKER (containers)**


### BlockchainOPS

BlcokchainOps:
- **Full Scale Operationalization Paradigm for Blockchain**
- It's application of **DevOps** in Blockchain lifecycle management. 

One can use **Kubernetes (CaaS)** & **Containerization (Docker)** to seamlessly *manage and govern* by orchasterating 
 - any **containerized Blockchain network** lifecycle with 
 	- the High availability, 
	- Auto Scalability, 
	- Self healing 
- any kind of **Blockchain workloads** 
	- Smart Contracts, 
	- Member registry,
	- et al


 



### When to use Which Framework

**Q. What Blockchain technology/framework should I choose on depending upon varying needs, such as** 
- public or private Network, 
- Permissioned Network or permissionless Network,
- Centralized ledger,
- Multi-party et al?
ANS: Blcokchain Frameworks do vary based on distinct needs. Here goes a quick look into the right framework from very many Blockchain technology options based on varying needs- 
- a **Centralized ledger** database {such as **Etherum (Public)/ AWS QLDB (Private)**},
- or a **Multi-party** {Channel Management for multiple stakeholder Scenario - such as **Hyperledger Fabric**}, 
- or a **Fully managed blockchain network** that helps eliminate intermediaries {such as, **AWS Managed Blockchian on HLF/EThrum**}

**Q. When to use Hyperledger Fabric & When to use Etherum?**
ANS: Hyperledger Fabric is well-suited for applications that require *stringent privacy and permission controls with a known set of members*.
- for example, a ```financial application``` where certain ```trade-related data is only shared with select banks``` 
	 
Whereas, Ethereum is well-suited for highly distributed blockchain networks where transparency of data for all members is important, 
- for example, a ```customer loyalty``` blockchain network that allows ```any retailer in the network to independently verify a user's activity across all members to redeem benefits```. 
- Ethereum can also be used for joining a public Ethereum blockchain network.

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
				
		
-Whereas "Blcokchain" is the Future network which answers aforemention inherent challanges with traditional SOR 
	- with *'Distributed' & 'Decentralized' Database/ Ledger Management system* 
	- wherein auditing, record keeping and **Data provenance** comes baked in 
```
	
	
SOR vs Blcokchain from **Business Network** standpoint:

|"Today’s Systems-of-Record" (Distributed Database or Ledger) | "Blcokchain" (The Future network of Distributed and Decentralized Database or Ledger)|
| :--: | :--: |
|<img src="/img/current_fin_network_SOR.png" width="300" Height="250" />|<img src="/img/future_net_BLOCHAIN.png" width="300" Height="250" />|
|Click on above image for full view|Click on above image for full view|
|**private programs** & **private Ledger** for Every participant | **shared programs** and **shared ledgers** for Every participant|


# Hyperledger Fabric HLF
- The Linux Foundation founded the Hyperledger project in Y2015 to advance **cross-industry** blockchain technologies. 
- HLF is one of the Framework from *"HL Framework & Tools ecosystem"* with the primary objective to provide **Permissioned with Channel Support**. i.e., HLF is one of the blockchain projects within Hyperledger.

- Like other blockchain technologies (Etherum), it also has 
	- a ledger, 
	- uses smart contracts, 
	- participants manage their transactions,
	- Data Provenance* by offering *immutable and cryptographically verifiable record of transactions* 
		
- Unlike other Blockchain technologies (Ethereum), it differs as
	- **private and permissioned**,
	- **No open permissionless system**,
	- **No unpermissioned entry** to any member/*unknown identities* to participate in the network,
	- **No PoW** ( “proof of work” protocol to validate transactions and secure the network),
	- **Membership Service Provider (MSP)**:  Restricted Entry to Members of a Hyperledger Fabric network enroll through a trusted MSP.

### Overview of Hyperledger Framework and Tools 

Broader ecosystem of *HL Framework & Tools:*

<img src="/img/HLBroaderView.png" width="800" Height="300" />

[Source](https://www.hyperledger.org/wp-content/uploads/2018/07/HL_Whitepaper_IntroductiontoHyperledger.pdf)



### Key Concpets of Hyperledger FABRIC
##### Blockchain network
	A blockchain network is a technical infrastructure that provides ledger and smart contract (chaincode) services to applications

##### Block and Chain 
	A block contains an ordered set of transactions. It is cryptographically linked to the preceding block, and in turn it is linked to be subsequent blocks.

	The ledger’s chain is a transaction log structured as hash-linked blocks of transactions. Suuch as, Blockchain B contains blocks 0, 1, 2.
	
##### Smart Contract
	A smart contract is code (invoked by a client application external to the blockchain network) that manages access and modifications to a set of *key-value pairs* in the *World State* via Transaction.

	
##### Chain Code

	In Hyperledger Fabric, smart contracts are packaged as chaincode. Chaincode is installed on peers and then defined and used on one or more channels.

##### World State

	*World state* maintains  “current state” of transaction in Ledger, and such data is stored in a state database for efficient reads and queries from chaincode. Supported databases include - *couchDB*.
	
##### Channel
	
	A channel is a private blockchain *overlay* which allows for data isolation and confidentiality. A channel-specific ledger is shared across the peers in the channel, and transacting parties must be authenticated to a channel in order to interact with it. Channels are defined by a *Configuration-Block*.
	
##### Membership Service Provider

	MSP refers to an abstract component of the system that provides credentials to clients, and peers for them to participate in HLF.

##### Ordering Service

	Also known as orderer. A defined collective of nodes that orders transactions into a block and then distributes blocks to connected peers for validation and commit. The ordering service exists independent of the peer processes and orders transactions on a first-come-first-serve basis for all channels on the network.


***
HLF also leverages *Gossip Protocol* & *Raft Algo* for following 3 major functions:
	- 1) manages peer discovery and channel membership; 
	- 2) disseminates ledger data across all peers on the channel; 
	- 3) syncs ledger state across all peers on the channel

The same *protocol* and *Algo* is used in **Progrium Consul** (a distributed computing CONSENSUS Algo for Leader election and worker management), and it is applied in Seneca (a Microservice Framework on Nodejs)
***

### Hyperledger FABRIC, Hyperledger COMPOSER, Hyperledger EXPLORER
**Hyperledger FABRIC:** 
```
- A very popular Blockchain Network from Hyperledger ecosystem. 
- Whereas other Blockchain Network from Hyperledger ecosystem, such as Hyperledger SAWTOOTH is the 2nd popular network.
```

**Hyperledger EXPLORER:**
```
User-friendly Web application tool from Hyperledger ecosystem to used to 
- view, invoke, deploy or query 
   - blocks,
   - transactions and associated data, 
   - network information (name, status, list of nodes), 
   - chain codes and transaction families, 
   - as well as any other relevant information stored in the ledger.
```
Reference: [Official Link](https://www.hyperledger.org/use/explorer)
Reference: [Video Demo](https://www.youtube.com/watch?v=mI6-qRagn_Q)

**Hyperledger COMPOSER:**
```
The Hyperledger Composer Playground provides a user interface for the 
- configuration, deployment and testing of a business network. 
- Advanced Playground features permit users to manage 
 	- the security of the business network, 
	- invite participants to business networks and 
	- connect to multiple blockchain business networks.
```
Reference: [Official Link](https://hyperledger.github.io/composer/latest/playground/playground-index)
Reference: [Video Demo](https://www.youtube.com/watch?v=gAxK6zYrfxI)

### DOCKER Hyperledger FABRIC Hyperledger EXPLORER
- [Fabric baseimage from hyperledger](https://github.com/hyperledger/fabric-baseimage)
- [Official reference](https://hyperledger-fabric.readthedocs.io/en/release-2.0/install.html)


***
<table>
  <tr>
    <td width="20%">
        <a href="https://www.hyperledger.org/use/explorer"> Hyperledger EXPLORER </a> Official Link of Hyperledger Explorer
    </td>
    <td width="30%">
        <a href="https://www.youtube.com/watch?v=mI6-qRagn_Q"><img src="img/HL_composer.png"></a>
    </td>
	    <td width="20%">
        <a href="https://hyperledger.github.io/composer/latest/playground/playground-index"> Hyperledger COMPOSER </a> Official Link of Hyperledger Composer
    </td>
    <td width="30%">
        <a href="https://www.youtube.com/watch?v=gAxK6zYrfxI"><img src="img/HL_explorer.png"></a>
    </td>
  </tr>
</table>


***

# AWS Quantum Ledger Database QLDB

### Overview of AWS QLBD
AWS QLDB
- provides a **centralized ledger** for auditing and record keeping purposes
- Offers **Verifiability** - verifies integrity of past records 

- is **Scalable**
- is **Serverless**
- can be provisoned with **AWS ClouFormation (IaC)** with additional user level control from clinet side with **IAM & ACL**

- can **trigger AWS Lambda events** to process other *downstream workflows* 
- can integrate with **other AWS PaaS Services**

### PYTHON client API for AWS QLDB

AWS QLDB supports low-level python client (AWS SDK for Python *Boto 3* API)

Using Python, one can perform following operations on Amazon QLDB
- Create a New Ledger
- Test Connectivity to the Ledger
- Create Tables, Indexes, and Sample Data
- Query the Tables in a Ledger
- Modify Documents in a Ledger
- View the Revision History for a Document
- Verify a Document in a Ledger

Please refer to the [link](https://docs.aws.amazon.com/qldb/latest/developerguide/getting-started.python.tutorial.html) for more details.
	


# AWS Managed Blcokchain AMB
Please refer [Live demo link](https://www.youtube.com/watch?v=WAIOBeQA2QQ) from 12MINS onward

### Key Concpets of AMB
Please Refer [Link for AMB Client Template](https://github.com/awslabs/amazon-managed-blockchain-client-templates)

# USE CASE IMPLEMENTATION

### Application of Blockchain for DATA TRUST in ENTERPRISE DATA ENGINEERING	

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

- for critical events/ datasets originating from **Streaming sources**	/ **Batch sources**
	```
	- for critical events originating from Streaming sources, such as "*credit* and *debit transactions* across bank accounts", and also
	- for critical datasets originating from Batch sources, such as "*history of assets* for Loan lending to Orgs/customers like vehicle maintenance records /or/ Lending application records".
	```


#### Solution Architecture using AWS QLDB

Architecture Solution using QLDB for above use case application:

<img src="/img/Architecture_QLDB_non-traditionalSOR.png" width="900" Height="500" />




### Application of Blockchain for CIRCULAR SUPPLY CHAIN	with IoT
Business Techo Problem statement 
- CIRCULAR SUPPLY CHAIN	with IoT
- Continuous Monitoring & Notification for SAFE ENVIRONMENTAL CONDITION for raw crop produce SHIPMENTs in TRANSPORATION
- right credit attribution to the Farmers

- Enabling **SMOOTH ADOPTION** of blockchain (HL FABRIC)
	- how to right size the load for blockchain?
	- How to cost optimize the adoption of blockchain?
	- how to manage, deploy, autoscale, descale container Blockchian network (HL FABRIC)?
	- how to monitor the nodes used for blockchain network cluster?
	- how to secure member's keys created for each member for accessing blockchain network? Possibly securing/fortifying keys in hardware using AWSCloud HSM.
	
*Please Note*
The fundatmental technology of blockchain is crpytography. Crptography works on KEYS. Hence, Keys become very important part of the solution.
	


#### Solution Architecture using HyperledgerFABRIC DOCKER AWS EKS IOT HSM

Architecture Solution using AWS Managed Blockchain for above use case application:

<img src="/img/IOTArchitecure.JPG" width="900" Height="500" />
Solution Architecture

# Reference
[1]https://www.youtube.com/watch?v=gAxK6zYrfxI

[2] https://www.youtube.com/watch?v=mI6-qRagn_Q

[3] https://www.youtube.com/watch?v=5CwIt-Alqhg

[4] https://www.youtube.com/watch?v=WAIOBeQA2QQ


# Contact info

Feel free to contact me to discuss any issues, questions, or comments.

My contact info can be found on my [GitHub page](https://github.com/DeepHiveMind).

# License

I, *The DeepHiveMind*, am providing code and resources in this repository to you under custom Copyright & license (Copyright 2019 DeepHiveMind & Creative Commons Legal Code CC0 1.0 Universal). Please Refer to the **[Copyright 2019 DeepHiveMind License]** for further details as to this. Thanks!
