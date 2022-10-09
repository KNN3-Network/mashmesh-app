# mashmesh-app

The project is a social discovery search engine built on the basis of Lens Protocol.
* We get the data of Profile NFTs and Follow (NFTs) from Lens Protocol, and tranform them into Graph-structured data. 
* Pagerank algorithm is used to calculate the rank score of the Profiles (Handle) to perform a new type of index from the perspective of network topology. 
* We make the social graph on Lens Protocol can be explored freely with Profiles as the vertices and Follows as edges.
* The Follow feature of Lens Protocol is intergrated, which enables users make new relationships during the social discovery.

You can view detailed codes of 
1. the graph visualization engine and data capture & processing in `/src/lib/knn3/graph.js`
2. the index based on PageRank algorithm in `/src/algorithm/pagerank.py`
3. the intergration of the Follow feature in `/src/contract/useLenshubContract.js`
and use the social discovery search engine in https://social.mashmesh.knn3.xyz/


## Introductory deck
Lens on MashMesh - Presentation slides (PDF version)

https://drive.google.com/file/d/19pCTFc0bXawAtDp_IO5-Qr-vuUe1qTaH/view?usp=sharing

Lens on MashMesh - Presentation slides (Google version)

https://docs.google.com/presentation/d/1eu_Ge8gx7RUiBMih-Rcnhx8vjBVVye2d2aoVSfdLLf0/edit?usp=sharing


## How to handle new data type (DCP, data collaborate mechanism backed by KNN3 Network)

As MashMesh is a open search protocol built on top of KNN3 Network - GraphX, instead of requiring every application to handle data fetching - indexing - Graph serving and other tedieous data process work, dapps can directly pulling any existing data from GraphX GraphQL. 

For these not existing new type data, for exampale, Polygon full node data (including NFTs & Tokens), Lens protocol social graph and lastest version of ENS, dapp developers can submit their data request through a EIP-style data integration mechanism, so called DCP (Data Collaboration Proposal) to KNN3 Network team, they can help you handle all the sophisticated data customization work right away (as long as the data type is on-chain or verifiable existed). 

For more details please go to: https://github.com/Web3-Data-Collaboration-Proposals/DCPs

In this Hackathon project, KNN3 Network help us handled

Polygon NFTs & Tokens: https://github.com/Web3-Data-Collaboration-Proposals/DCPs/blob/published/DCPs/DCP-8.md

Lens Protocol social graph (ProfileNFT & FollowingNFT): 

Latest ENS integration: 

It actually helps our dev experience much simpler!


## Install dependencies

`pnpm i`

## Start App

`pnpm dev`

Please make sure your wallet is connecting polygon network, then you can start playing.

