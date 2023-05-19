---
title: "Building Subgraphs: A Guide to Understanding and Creating Them"
seoTitle: "Building Subgraph: A Guide to understanding and creating them"
seoDescription: "Discover the world of subgraph development and learn how to create powerful subgraphs in this comprehensive guide."
datePublished: Fri May 19 2023 04:10:29 GMT+0000 (Coordinated Universal Time)
cuid: clhu1lu1v000209l01jtbgirx
slug: building-subgraphs-a-guide-to-understanding-and-creating-them
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1684469137111/bc252cd0-be9f-4523-b4a8-ffd8421534d8.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1684469232289/f72272c7-89c4-411e-b72b-4ac0622c5fc5.png
tags: data-science, blockchain, web3, thegraph

---

In the first article, we explored the significance of data in the blockchain ecosystem and the transformative role of The Graph in facilitating data access for decentralized applications (DApps). The second article provided an overview of The Graph's decentralized network, highlighting the various participants and their collaborative efforts in maintaining network operations. In this third article, our focus will be on understanding subgraphs, setting up the required tools on our local machine, and building a basic subgraph for an ERC20 token. So let's get started.

### What is a subgraph?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683521055084/6f15278f-1e1a-472f-b6e1-87b16471a208.png align="center")

**Subgraph** - the mysterious buzzword that's been popping up everywhere in each of our articles. But is a subgraph like a mini-map for blockchain data, or more like a GPS for developers who are lost in the blockchain wilderness? Is it a group of superheroes who band together to fight blockchain villains, who organize and analyze blockchain data? Is it like little black boxes that you can store all your blockchain data in, or more like tiny submarines that can dive deep into the data ocean and retrieve specific pieces of information? What it is? Your head might be floated with similar kinds of questions. Let's try to answer these questions.

Imagine you have a massive library with thousands of books, and you want to create an index to help readers find specific books more easily. To do this, you might create an index page that lists all the books in the library, grouped by author or subject, along with their location on the shelves. Each book in the library would have its entry on the index page, with all its relevant details like author name, title, genre, and publication date. In the same way, a subgraph is like an index page for a specific set of data on the blockchain. A subgraph is an open **API** that defines how to ingest, index and serve data. A subgraph extract data from the blockchain, process it and stores it so that it can be easily queried via **GraphQL**. Developers use subgraphs to feed data to the front-end interface of their application. Developers define the criteria for the index by writing a GraphQL schema, and mapping functions are created to extract and map the relevant data to the schema. The subgraph is then deployed and made available for other developers to use, making it easier for them to find and use specific data on the blockchain.

### Technical Prerequisites for Getting Started with Subgraph Development

Before diving into subgraph development, it's essential to have a solid understanding of the technical prerequisites. These prerequisites will equip you with the necessary knowledge and tools to effectively build subgraphs and harness the power of The Graph protocol.

1. GraphQL Fundamentals: To work with subgraphs effectively, it's essential to understand GraphQL, the query language for APIs. Familiarize yourself with GraphQL concepts like schemas, types, queries, and mutations. The official [GraphQL](https://graphql.org/learn/) website provides comprehensive documentation and tutorials. If
    
    you prefer video tutorials, [this](https://youtu.be/yqWzCV0kU_c) beginner-friendly video tutorial offers a great introduction to GraphQL.
    
2. AssemblyScript: AssemblyScript is a programming language that aims to provide a subset of the JavaScript/TypeScript syntax while allowing for direct compilation to WebAssembly. It can be seen as a variant of TypeScript that focuses on generating efficient WebAssembly code. AssemblyScript shares similarities with TypeScript, making it familiar to developers already experienced with JavaScript or TypeScript. AssemblyScript is stricter than normal TypeScript, yet provides a familiar syntax. During the subgraph development, we use AssemblyScript is used to write mapping functions. The mappings take data from a particular source and transform it into entities that are defined within our schema.
    
3. Smart Contract: Subgraphs often interact with data stored in smart contracts on the blockchain. So having a good understanding of smart contracts is always good. As a subgraph developer, we do not need to understand the whole smart contract, we need to understand just enough to be able to capture data for interaction. Key areas of focus for subgraph developers when dealing with smart contracts include:
    

* **Finding the core contract:** Decentralized applications (DApps) typically consist of multiple smart contracts that communicate with one another. In most scenarios, there is a central contract that serves as the core of the application, responsible for updating user state and managing key functionalities. Understanding and interacting with this core contract is crucial for subgraph developers when working with DApps. By focusing on the core contract, subgraph developers can effectively capture and process the relevant data and events necessary for their subgraph's functionality and integration with the DApp.
    
* **State Variables**: Identify the state variables that hold critical information within the contract. These variables may represent balances, ownership details, or other important data points. Consider capturing and representing them accurately in your subgraph.
    
* **Contract Functions**: Understand the various functions defined within the contract. Pay attention to the input parameters, return values, and the purpose of each function. This will help you identify the relevant data and events to capture in your subgraph.
    
* **Event Emission**: Look for events emitted by the contract. Events are crucial for capturing important state changes and updates within the contract. Analyze the event structures, including their parameters and data types.
    
* **Contract Upgradability**: If the contract has provisions for upgradability or proxy patterns, be aware of how it affects data access and storage.
    
    By focusing on these aspects while reading a smart contract, you can gain a comprehensive understanding of its structure, functionality, and data flow. This knowledge will guide you in accurately capturing and representing the relevant data within your subgraph.
    

By meeting these technical prerequisites and utilizing the recommended sources, you'll be well-prepared to embark on your subgraph development journey, harnessing The Graph's capabilities to index and query data from decentralized applications.

### Setting up Your Environment for Subgraph Development

Before we dive into building our subgraph, it's important to ensure we have the necessary tools installed on our local machine. In the next article, we will guide you through the process of developing your subgraph. But for now, let's focus on installing the required tools so that we can get started. By having the necessary tools installed, we can work efficiently and effectively. This ensures that we can build a quality subgraph without any unnecessary delays or issues. So, let's take a step back and ensure that we have everything set up correctly before we start building our subgraph.

Before proceeding with the installation of any other tools required for subgraph development, it is essential to check if Node.js is already installed on your local machine. If you do not already have Node.js installed on your local machine, you can download and install the latest version from the [official website](https://nodejs.org/en/download). Once installed, you can check if Node.js is properly installed on your machine by running the following command in your terminal:

```bash
node -v
```

This command will display the version of Node.js installed on your machine. If a version number is displayed, then Node.js is properly installed and configured on your machine, and you can proceed with the installation of other tools required for subgraph development.

If Node.js is not installed or if an error message is displayed, you will need to download and install Node.js before proceeding with subgraph development. By ensuring that Node.js is installed correctly, you can ensure that you have a stable foundation for subgraph development.

Once you have installed Node.js and npm, you can proceed to install the Graph CLI tool. This tool enables developers to create and manage subgraphs easily. You can install the Graph CLI by running the following command in your terminal:

To install **The Graph CLI** with npm:

```bash
npm install -g @graphprotocol/graph-cli
```

To install **The Graph CLI** with yarn:

```bash
yarn global add @graphprotocol/graph-cli
```

To check if The Graph CLI is installed on your local machine, you can run the following command in your terminal.

```bash
graph --version
```

By checking if The Graph CLI is installed on your local machine, you can ensure that you have access to the necessary tools for subgraph development. The Graph CLI is an essential tool for subgraph development as it allows you to create, deploy and manage subgraphs on The Graph Network.

we have successfully set up our local machines and installed all the necessary tools required to kickstart our subgraph development process. With everything in place, we are now ready to delve into the practical aspects of subgraph development. In our next article, we will embark on the exciting task of building a subgraph for an ERC20 token. This hands-on experience will allow us to apply the knowledge we've gained and witness firsthand the power and versatility of subgraphs in capturing and processing data from smart contracts. Stay tuned for an immersive and insightful exploration into the world of subgraph development.

---

If you enjoyed reading my blog, I would greatly appreciate it if you could take a moment to show your support by liking and commenting on it. Your feedback and engagement are incredibly valuable to me and will help me to continue improving and creating content that is informative and engaging. I'll be making a bit of content for The Graph in the coming days. Follow me on Twitter and Hashnode to be alerted about my next article in this series. In the next article, we build our first subgraph. You can find me on all platforms @subgraphdev

---