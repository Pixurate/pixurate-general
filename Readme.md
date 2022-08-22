## Inspiration
I read an article about today's web2 user review systems and how they are widely manipulated. Immediately, I thought of keeping all reviews on the blockchain transparently and securely. The friction is that online stores incur high development costs and customers need better incentives to leave feedback on blockchain tech. So we decided to create Pixurate, a web3 application easily integrated into web2 websites and more engageable by web2 users.

## What Pixurate does
It creates AI-powered-NFTs from an image of each order with purchase metadata. Pixurate NFTs are unique for each purchase and prove the order. NFT owners can leave a review for these orders/products with purchase verification on the blockchain. Pixurate stores these user reviews on blockchain transparently.

## How we built it
- Firstly, we created widgets easily embeddable into online shops to engage customers.
- We created a plugin for Salesforce Commerce Cloud (Next plugins are coming for Shopify, Magento, WordPress, etc.)
- Then, we created some API endpoints to collect orders and collected order data for NFT creation
- We generated images for products with AI, minted NFTs with these images, and delivered these images to customers.
- Then, we sent emails to these customers to leave reviews for these products and collect reviews.

## Challenges we ran into
- AI image generation
- To find engagement ways for our customers to web3

## Accomplishments that we're proud of
- We believe that we created the future of the user review systems built on the blockchain with order proofs. It is a unique idea, and we believe we will change review systems.

## What we learned
- While building our application, we used products of Hackathon sponsors, and we learned many different web3 tools while integrating these products into our application. These tools boosted our development process and helped us create a more solid application.

## What's next for Pixurate
It is an MVP at the moment, and many improvements are on the way. Our first purpose is to make this application sellable and bug-free. Then, we plan to improve AI-generated images and integrate them with more solid AI models. 

We have already developed a Salesforce Commerce Cloud plugin and plan to implement new plugins for other e-commerce platforms like Shopify, WooCommerce, Magento, etc, to expand our integration with Web2.

# PIXURATE PROJECT DETAIL

**This product is an MVP**

Pixurate is developing **a review system on blockchain** for eCommerce owners to **boost their engagement** and **collect authentic reviews.**

## WHY WE BUILD IT

**Blockchain** can bring extraordinary transparency to review systems and provide users with the most accurate information. In the **WEB2** world, all reviews are stored in 3rd party or in-house databases, and this information can be **easily manipulated**. Moreover, **even the industry leader, Trustpilot**, cannot offer a secure order verification mechanism. From this point of view, **we decided to develop the web3 version of Trustpilot**and **our WEB3 approach solves the problem in all its aspects in a magical way by using web3.**

### PROBLEM

eCommerce owners suffer from:
- Low customer engagement: People only tend to leave a review for bad experiences,
- Fabricated reviews: bots contaminate and manipulate review and rating systems,
- High investment requirements for firms to enter web3,
- Need for credible, authentic testimonials and widgets that show their quality.

### SOLUTION

Pixurate:
- Builds the most trustable and original order verification system using blockchain
- Boosts customer engagement with NFTs and incentivizes feedback contribution with token rewards
- Generates AI-powered NFTs for websites without huge development expenses
- Provides websites with integrable widgets for reviews, ratings, testimonials, and marketing.

### HACKATHON TRACKS

Pixurate addresses three tracks on Polygon Hackathon. 
Our main track is the Web3 integration of user review systems on eCommerce platforms.

Web3 Integration in Web2 - Pixurate provides seamless integration with Web2 eCommerce platforms. With Pixurate integration, online purchases are awarded unique NFTs that include the purchase metadata. These NFTs prove the verification of NFT owners on the blockchain. Verified NFT users' feedback on the Pixurate platform is stored and visible on the blockchain, providing a transparent and secure version of user review systems.

Nfts - Pixurate generates AI-powered NFTs of physical products purchased online. Each Pixurate NFT represents a specific purchase with its metadata. Users store their NFTs on the Pixurate app and give feedback on their purchases. Pixurate NFTs can be shared on social media for interaction. NFT owners are eligible for awards for their engagement. 

Public Goods - Pixurate offers an innovative Web3 application to solve the problems of review manipulation and consumer rights to share and access authentic consumer experiences. Pixurate review system is a 3rd party organization with no conflict of interest in revealing accurate information and applies the highest level of purchase verification. Pixurate does not allow fake/bot reviews, review censoring, and manipulation by design. Pixurate's indirect incentive mechanism motivates the consumers to share their experiences and facilitates revealing the highest quality information about online shops.

## HOW IT WORKS

1. It is enough to install our plugin or widget on an eCommerce platform to generate unique NFTs.
2. When an order is completed, our plugin/widget informs us of all order information and generates an NFT that includes this order information
3. We display to the customer her/his NFTs for each product that he ordered by using a widget on the order confirmation, and the customer can easily see his NFT detail.
4. If the customer already has an account or has created an account and connected his wallet, we are transferring this NFT to his account. (In the future, we can create a separate wallet for each customer.)
5. If a customer adds a review for this product, we store this review for a while (Because we are giving some time to the customer if she/he changes her/his mind) and then generate metadata information that also includes this review and stores it on **IPFS**.
6. We are putting **IPFS URL** that includes customer review and marking this NFT as reviewed on Smart Contract that we deployed (Currently, we are not storing images on IPFS, but we will do it asap)
7. Then, customers' reviews can be displayed on the blockchain, and also eCommerce shop display all the reviews by using our widget.

You also want to check this URL:
[https://miro.com/app/board/uXjVOrJHcOg=/?share_link_id=132326004962]

## WHAT IS THE ARCHITECTURE OF THE APPLICATION

Currently, we are not using precisely this architecture, but in a short time, we will completely use this microservice architecture. (We developed this project ~45 days as a side project as two developers, and as you guess, we need more time for this complex architecture.)

![Software Architecture](https://i.ibb.co/7tNMjX4/software-architecture.jpg)

## TECHNOLOGIES THAT WE USED

- Solidity : For coding smart contract
- Reactjs : For creating user widgets
- Nodejs : For interacting with smart contract
- PHP : For Core User application
- Vuejs: For our dashboards
- Nextjs: For our Homepage
- Salesforce Commerce Cloud: For demo shop and creating our first plugin for 3th parties
- IPFS: via NFT.Storage **(Eligibility For sponsorship prize)**
- Sequence: For connecting user wallets **(Eligibility For sponsorship prize)**
- AWS: For storing images and calculating rating average via Lambda function **(Eligibility For sponsorship prize)**
- Spheron: To deploy our home website **(Eligibility For sponsorship prize)**
- Metamask: For connecting user wallets

## HOW THE CODE WORKS

We tried to collect all repos under a single repo to make the review process easier by using **Git Submodules**. You can find how each repo is working here:

### NFTURATE

It is our Core application for authentication, displaying dashboards, collecting reviews, and serving widgets. It collects all requests from users and distributes each request to the service that is responsible for it. It is written with PHP and VueJS. (Laravel)

### PIXURATE WIDGETS

It is a reactjs repo that includes all widgets that we created. They can be used alone or can be used by a plugin that we created. (Like PIXURATE-SFRA-CARTRIDGE).
### PIXURATE-HOME-Nextjs

It is our homepage repo and written in NEXTjs and deployed via Spheron

### PIXURATE-MINTING-SERVICE

It is a nodejs application that interacts with smart contracts by using Etherjs. We are aware that there are some security issues there, but they will be fixed when this project is industrialized.

### PIXURATE-SMART*CONTRACTS

It is the code that we developed as a smart contract.
Contract address: 0xf2EcC77c1F1fe940E800C841910EE3c436f26B58

### PIXURATE-SFRA-CARTRIDGE

It is Salesforce Commerce Cloud Plugin that integrates our service with Salesforce Commerce Cloud, So ecommerce shop owners can easily install it. We are planning to create plugins like that for Shopify, WooCommerce, Magento, Ikas.

Demo shop address and Credentials are in the private repo and you can find details are there. It is private because of SFCC instance capacity is so limited and expensive :)

