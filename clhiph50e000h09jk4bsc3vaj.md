---
title: "A brief overview of The Graph Network and its Participants."
seoTitle: "A brief overview of The Graph Network and its Participants."
seoDescription: "Explore and how The Graph Networks works  and how each participant works together."
datePublished: Thu May 11 2023 05:45:26 GMT+0000 (Coordinated Universal Time)
cuid: clhiph50e000h09jk4bsc3vaj
slug: a-brief-overview-of-the-graph-network-and-its-participants
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1687582050663/4ffb690a-5924-4303-8498-6ff100330417.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1683783756413/5bfd10ac-9e7b-4ce1-89d1-2ff68e22c4fb.png
tags: data-science, graphql, blockchain, web3, thegraph

---

In the first article of this series, we discussed the importance of data in the blockchain ecosystem and how The Graph is revolutionizing the way decentralized applications (DApps) access and use that data. We learned that The Graph is a decentralized indexing and querying protocol that provides developers with a powerful tool for accessing and processing data from various blockchains. We also learned the benefits of using The Graph for developers, such as improved scalability, faster development cycles, and more efficient data querying. Overall, the last article highlighted The Graph's potential to unlock the full potential of blockchain data, making it more accessible and useful for developers building the next generation of DApps. In this article, we are going to continue our journey of understanding **The Graph protocol** in depth.

The Graph protocol enables the indexing and querying of blockchain data by providing developers with a powerful infrastructure that allows them to index, search, and retrieve data from various blockchains. The protocol works by creating **subgraphs**, which are essentially custom indexes that developers can use to organize and access specific data on the blockchain. These subgraphs are created using a set of open-source tools and APIs provided by The Graph protocol, allowing developers to easily create and deploy their subgraphs. Once a subgraph is created, it can be queried using **GraphQL**, a query language that enables developers to retrieve only the data they need. By providing this infrastructure, The Graph protocol allows developers to efficiently retrieve data from blockchains without having to run their nodes, enabling them to focus on building the front-end interface of their DApps.The use of The Graph protocol also helps to reduce the load on the Ethereum network by reducing the number of requests being made to full nodes. Many popular DApps are using The Graph, One of the major DApps using The Graph protocol is Uniswap, a decentralized exchange that allows users to swap cryptocurrencies without the need for a centralized intermediary. Uniswap uses The Graph to retrieve and organize data about token pairs, liquidity pools, and trading volumes. Another significant DApp using The Graph is Compound, a decentralized lending platform that enables users to borrow and lend cryptocurrencies. By leveraging The Graph protocol, the Compound can efficiently query data on lending and borrowing rates, collateral ratios, and transaction history. Additionally, Aave, another decentralized lending platform, also uses The Graph to index and query data related to borrowing and lending activities. You can find the list of all subgraphs built on The Graph [here](https://thegraph.com/explorer).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683513650798/967daca1-584e-44c2-86bb-1f53cdc7788f.png align="center")

### How does The Graph Network work?

The Graph protocol uses a decentralized network of nodes to index and query blockchain data. The Graph learns what and how to index blockchain data based on the subgraph. When a developer wants to create a **subgraph**, they use The Graph's open-source tools and APIs to define the data they want to index and the schema for how that data should be organized. The subgraph is then deployed to a network of nodes, which work together to index the specified data on the blockchain. These nodes are incentivized to perform this work through a system of rewards paid in Graph Tokens (GRT), which is the native cryptocurrency of The Graph protocol. Once a subgraph is indexed, developers can use GraphQL to query the subgraph and retrieve the specific data they need, such as transactions, smart contract events, or user balances. Let's try to understand the whole process in simple steps.

**The Flow**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683521251885/914c3268-7096-472d-8301-fe52015a8568.png align="center")

1. The Dapps add data to the blockchain through a transaction on a smart contract.
    
2. Smart contracts emit one or more events while processing the transactions.
    
3. Graph nodes continuously scan the Ethereum for new blocks and the data for your subgraph they may contain.
    
4. Graph nodes find Ethereum events for your subgraph in the blocks and use handlers defined in the subgraph to create or update data.
    
5. Dapps can query these data using the GraphQL endpoint.
    

The Graph Network is a decentralized ecosystem and, it has three main participants: **Indexers, Curators, and Delegators**, others are **Fishermen**, **Arbitrators** and **Subgraph Developers**. By working together, these participants ensure that developers have access to reliable and accurate data and that users can access and interact with decentralized applications seamlessly.

**An overview of how all participants work together**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683781249215/1d9a1405-2572-4b01-80c5-be7aae53c2d0.png align="center")

We'll explore the functions and responsibilities of all the different participants in The Graph network, including Indexers, Curators, Delegators, Fishermen, Arbitrators, and Subgraph Developers. By gaining a deeper understanding of the roles each participant plays and how they interact with one another, we can better appreciate the decentralized nature and overall efficiency of The Graph network. From maintaining the accuracy and reliability of indexed data to building and updating subgraphs, each participant plays a critical role in enabling developers to build more powerful decentralized applications on the blockchain. By working together in a transparent and decentralized environment, The Graph network participants are contributing to the growth and success of the blockchain ecosystem as a whole. Let's explore each participant's role one by one:

**Indexers:** Indexers are nodes on the network that index blockchain data and make it available for querying. They are responsible for running and maintaining the indexing software, which involves monitoring the blockchain for new data, extracting the relevant data, and storing it in a format that can be easily queried. Indexers also stake tokens to participate in the network, which serves as collateral and incentivizes them to provide reliable and accurate indexing services. In order to run an indexing node, Indexers must stake 100,000 GRT or more with the network.

Indexers earn rewards for indexing data and serving queries. The amount of rewards they earn is proportional to the amount of data they index and the number of queries they serve. Indexers are also incentivized to ensure their indexes are accurate and up-to-date, as any inaccuracies or missing data can result in penalties or reduced rewards.

**Curators:** Curators are individuals or entities that signal their interest in specific subgraphs by staking tokens. They are responsible for identifying high-quality subgraphs and signaling their value to the network. Curators can signal their interest in subgraphs created by indexers or other curators.

Curators earn rewards for curating valuable subgraphs. The amount of rewards they earn is proportional to the number of tokens they've staked. Curators are incentivized to identify and signal high-quality subgraphs, as doing so can attract more users and increase the value of the network.

**Delegators:** Delegators stake tokens to support specific indexers or curators. By doing so, they earn a portion of the rewards earned by those indexers or curators. Delegators do not perform any work on the network themselves, but they provide critical support to other participants.

Delegators can choose to support specific indexers or curators based on factors such as their track record, the quality of their work, and their potential for future success. Delegators can also change their support at any time, providing flexibility and allowing them to adapt to changing conditions in the network.

**Fisherman:** Fishermen serve as a kind of "watchdog" to ensure the accuracy and reliability of indexed data. Fishermen monitor the network for any errors, inaccuracies, or malicious behavior by indexers, and submit evidence of any such behavior to the network. This evidence is then used to penalize the offending indexer and compensate the Fisherman with a portion of the penalty.

Fishermen earn rewards for submitting valid evidence of misconduct by indexers. The amount of rewards they earn is proportional to the severity of the offense and the amount of penalties imposed on the offending indexer. By serving as a check on the behavior of indexers, Fishermen play a critical role in maintaining the accuracy and reliability of The Graph Network, which benefits developers, users, and other stakeholders in the blockchain ecosystem.

**Arbitrators:** Arbitrators are responsible for resolving disputes that arise between indexers and curators. They review evidence submitted by Fishermen and other parties and determine whether a penalty should be imposed on an indexer or curator, and if so, the amount of the penalty.

Arbitrators earn rewards for their work in resolving disputes. The amount of rewards they earn is proportional to the number and complexity of disputes they resolve. Arbitrators are incentivized to be fair and impartial in their decisions, as any appearance of bias or favoritism could damage their reputation and lead to fewer opportunities to work as an arbitrator in the future. Arbitrators play a critical role in ensuring the integrity and fairness of The Graph Network, which benefits all participants and contributes to the growth and success of the blockchain ecosystem.

**Subgraph Developers:** Subgraph Developers are participants in The Graph Network that are responsible for creating and maintaining subgraphs, which are used to index and query specific data on the blockchain. Subgraph Developers use The Graph's tools and infrastructure to build and deploy subgraphs and are responsible for keeping them up-to-date and accurate.

Subgraph Developers in The Graph Network earn by building the subgraph for Dapps. Subgraph Developers can also earn additional rewards by participating in The Graph's grant programs, which provide funding for the development of new subgraphs that meet specific criteria or address specific needs within the decentralized application ecosystem.

In summary, The Graph Network is a decentralized ecosystem in which indexers, curators, and delegators work together to index and query blockchain data. Indexers are responsible for indexing data and serving queries, curators are responsible for identifying valuable subgraphs, and delegators provide support to other participants by staking tokens. By working together, these participants ensure the efficient and effective operation of The Graph Network, which benefits developers, users, and other stakeholders in the blockchain ecosystem.

---

If you enjoyed reading my blog, I would greatly appreciate it if you could take a moment to show your support by liking and commenting on it. Your feedback and engagement are incredibly valuable to me and will help me to continue improving and creating content that is informative and engaging. I'll be making a bit of content for The Graph in the coming days. Follow me on [Twitter](https://twitter.com/subgraphdev) and Hashnode to be alerted about my next article in this series. In the next article, we will explore the subgraphs and how the subgraphs are built. You can find me on all platforms **.@subgraphdev**.

---