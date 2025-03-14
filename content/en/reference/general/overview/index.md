---
title: "Overview"
description: "Helpful reference materials for the Filecoin specification, implementations, and ecosystem."
lead: "Helpful reference materials for the Filecoin specification, implementations, and ecosystem."
draft: false
images: []
type: docs
menu:
  reference:
    parent: "reference-general"
    identifier: "overview-b01c7433c7ec0d15d289049cd501d613"
weight: 10
toc: true
aliases:
    - "/reference"
    - "/reference/general"
    - "/build/developer-tools/wallets-signing-tools-api-clients/"
    - "/build/signing-libraries/"
    - "/reference/reference/overview/"
---

## About Filecoin

- [**Filecoin Specification**](https://spec.filecoin.io/) - technical specification for Filecoin protocol and its associated subsystems.
- [**Engineering Filecoin's Economy**](https://filecoin.io/2020-engineering-filecoins-economy-en.pdf) -  the design of Filecoin's economic incentives.
- [**Filecoin Slack**](https://filecoin.io/slack) - announcement, open discussion of Filecoin.
- [**Filecoin Community**](https://github.com/filecoin-project/community) - Filecoin community and ecosystem channels, discussion forums, and more.
- [**Filecoin 中文社区**](https://github.com/filecoin-project/community-china) - resources and forum for the Chinese community, maintained and moderated by CoinSummer & PL.
- [**Filecoin YouTube channel**](https://www.youtube.com/channel/UCPyYmtJYQwxM-EUyRUTp5DA) -  various Filecoin workshops, conference talks, and meetups.

## Filecoin Network

### Node implementations

- [**Lotus**](https://github.com/filecoin-project/lotus) - _**Recommended**_  most advanced implementation and [security audited](https://spec.filecoin.io/#section-intro.implementations-status), in GoLang.
- Other implementations (In progress):
  - [Fuhon](https://github.com/filecoin-project/cpp-filecoin) - C++
  - [Forest](https://github.com/ChainSafe/forest) - Rust
  - [Venus](https://github.com/filecoin-project/venus) (formerly `go-filecoin`) - also in GoLang ([Venus documentation](https://venus.filecoin.io/)).

- Lotus Docker Hub Images (unofficial):
  - [`glif/lotus`](https://github.com/glifio/filecoin-docker)
  - [`ognots/lotus`](https://hub.docker.com/r/ognots/lotus) - `mainnet-v1.830-rc1`
  - [`textile/lotus`](https://hub.docker.com/r/textile/lotus) - latest

### Networks

[`network.filecoin.io`](https://network.filecoin.io) - lists all current Filecoin networks and related information.

- **Mainnet**
  - [Mainnet network status](https://filecoin.statuspage.io/) - reports the status and incident of the Filecoin Mainnet.
- **Calibration**
  - Largest testnet which support 32 GiB and 64 GiB sectors.
  - See [`#fil-net-calibration-announce`](https://filecoinproject.slack.com/archives/C01C5PT7ETC) for announcements and [`#fil-net-calibration-discuss`](https://filecoinproject.slack.com/archives/C01D42NNLMS) for questions and discussion in [Filecoin Slack](https://filecoin.io/slack).
- **Local Devnet**
  - [Run a Local Devnet using Lotus](https://lotus.filecoin.io/lotus/developers/local-network/).
  - [Textile's local devnet](https://docs.textile.io/powergate/localnet/#localnet-with-lotus-client) -  uses a mocked sector builder for faster deal confirmation and it is for storage app prototyping.
  - [Ganache for Filecoin](https://www.trufflesuite.com/docs/filecoin/ganache/overview) - local network to support development with Filecoin by various ways.

## Network status

Tools to check status and details of the network and chain.

### Block explorers

- [`Filfox.info`](https://filfox.info/en) -  Mainnet
- [Filscan](https://filscan.io) -  Mainnet & Calibration
- [Grafana](https://stats.filecoin.io/) - Network Statistics Dashboard
  - [Mainnet](https://stats.filecoin.io/)
  - [Calibration](https://stats.calibration.fildev.network/d/z6FtI92Zz/chain?orgId=1&refresh=25s&from=now-30m&to=now&kiosk)

### Chain data and monitoring

- [`dashboard.starboard.ventures`](https://dashboard.starboard.ventures/) - network health monitoring
- [Filstats.io](https://filstats.io) - node telemetry monitoring - add your node!
- Orphan blocks (not an official protocol term in the Filecoin Spec) - Blocks without rewards that were either mined on the wrong tipset that the network fails to deliver in time, or a mix resulting in reorgs.
- [Sentinel Project](https://lilium.sh/) - Filecoin Network Monitoring and Analysis System

### Storage/Deals status

- [`storage.filecoin.io`](https://storage.filecoin.io/) - general storage summary of Filecoin
- [`filecoin.tools`](https://filecoin.tools) - check your CID's storage deal status. Also provides an API - check [`filecoin.tools/docs`](https://filecoin.tools/docs) for reference
- [`file.app`](https://file.app/) - Filecoin storage provider analytics
- [Deals list at `Filfox.io`](https://filfox.info/en/deal)

## Storage Web Applications

Web-based applications that store your data on Filecoin. No command-line or coding experience required.

- [Estuary](https://estuary.tech) allows uploading and storing content on the Filecoin network directly from your browser. Allows anyone with public data to store and retrieve using a few API calls.
- [**Slate.host**](https://slate.host) - a storage application on Filecoin to collect, organize, and link files together and share them, listed on [Product Hunt here](https://www.producthunt.com/posts/slate-f195dcdd-18e2-4dc2-8c70-45208ccbb862) on GitHub at [`filecoin-project/slate`](https://github.com/filecoin-project/slate/)
- [ChainSafe Files](https://files.chainsafe.io/) - Dropbox-style UI, login with OAuth or general MetaMask
- [`File.video`](https://file.video/) - video hosting with decentralized transcoding from LivePeer
- [Starling Framework for Data Integrity](https://www.starlinglab.org/)
  - to securely capture, store and verify human history
  - learn more at [`starlinglab.org/78days`](https://www.starlinglab.org/78days/) or the [Filecoin blog interview](https://filecoin.io/blog/starling-framework/)
  - [`Starlingstorage.io`](https://starlingstorage.io/) - API + CLI that simplified storing data to a local Lotus node for preservation use cases.

## APIs & Developer tools

Developer tools, API clients & storage services that developers can use to build on Filecoin.

### Storage APIs for app builders

- [Estuary](https://estuary.tech) - a simple IPFS node that integrates with Filecoin. For infrastructure operators, developers and users.
  - [Estuary documentation](https://docs.estuary.tech)
  - [Estuary www](https://github.com/application-research/estuary-www) - a simple web app example
  - [Estuary Rclone](https://docs.estuary.tech/Learn/tutorial-managing-files-with-rclone) - sync to and from different cloud storage providers and Estuary
- [`NFT.storage`](https://nft.storage/) - beta service from Protocol Labs for storing off-chain _NFT_ data on IPFS and Filecoin.
- [`Web3.storage`](https://web3.storage/) - beta service from Protocol Labs for storing off-chain _dApp_ data on IPFS and Filecoin, with help from Pinata (a fast IPFS Pinning Service) to [distribute the content across IPFS](https://www.pinata.cloud/blog/protocol-labs-and-pinata)
- [`Slate.host`](https://github.com/filecoin-project/slate/#developer-api) - has a Developer API that allows you upload files with an account
- [`Textile.io's tools`](https://docs.textile.io/) - suite of tools for interacting with IPFS and Filecoin
  - includes The Hub, Buckets, ThreadsDB, Powergate, [Tableland](https://blog.textile.io/tableland-is-coming-build-web3-with-sql/) (new) and Filecoin bridges to Polygon and NEAR
  - [Powergate](https://docs.textile.io/powergate/) - infrastructure tool for using IPFS for hot storage and retrieval and Filecoin for cold, with deal helpers and other convenience features
  - [Textile Buckets](https://docs.textile.io/buckets/) - simplified cloud bucket store on IPFS with archive to Filecoin option using Powergate under the hood
- [Fleek's tools](https://fleek.co/) - provides access to Fleek's hosted services using IPFS, Textile, Filecoin, Ethereum, etc.
  - [Space SDK](https://docs.fleek.co/space-sdk/overview/) -  modular JavaScript/Typescript library and set of interfaces that packages tools and features enabled by Open Web protocols like IPFS, Textile, Filecoin, and Ethereum.
  - [Space Daemon](https://docs.fleek.co/space-daemon/overview/) - packages together IPFS, Textile Threads and Buckets, and Textile Powergate into one easy to install background service

### Message signing tools

- [Filecoin Signing Tools](https://github.com/Zondax/filecoin-signing-tools) - _**Recommended**_ a pure JS or Rust / WASM / JSONRPC library for creating signed messages apart from a Filecoin node.
  - Also available on npm at [`@zondax/filecoin-signing-tools`](https://www.npmjs.com/package/@zondax/filecoin-signing-tools)
  - For an open source example of how to use it see the [Glif web wallet](https://github.com/glifio/wallet) on GitHub.
- [Filecoin JS Signer](https://github.com/blitslabs/filecoin-js-signer) - [_last update: June 2021_] pure TS / JS library for creating signed messages and interacting with Filecoin's built-in Actors (like Payment Channel and Multisig), used by the [Filecoin Loans grant project](https://github.com/blitslabs/filecoin.loans-monorepo).
  - On npm at [`@blitslabs/filecoin-js-signer`](https://www.npmjs.com/package/@blitslabs/filecoin-js-signer)

### Wallet-related tools

- [Filecoin Rosetta API Proxy](https://github.com/Zondax/rosetta-filecoin) - [Rosetta](https://www.rosetta-api.org/) is an API standard created by Coinbase for a consistent interface to many chains for wallets and exchanges.
- [FilSnap MetaMask Plugin](https://metamask.io/flask/) - MetaMask has a new plugin system currently still in beta that developers can try out. The MM UI will not change but Filecoin keys are in the MM vault. Try it with <https://filsnap.chainsafe.io/>

### Node Infrastructure & APIs

> NOTE: making deep calls into the chain’s history may take some time to return and it may be more efficient to use a chain database (e.g. used by block explorers) that stores the chain’s history and is optimized for queries.

- [Glif nodes](https://lotus.filecoin.io/lotus/developers/glif-nodes/) and [Infura](https://docs.infura.io/infura/networks/filecoin) - Hosted endpoints to Filecoin mainnet and testnet.
  - These endpoints support read-only calls and `MPoolPush()` for sending signed transactions to the network (which can be signed using the [Message signing tools](#message-signing-tools)).
- [**Lotus JSON-RPC API**](https://lotus.filecoin.io/lotus/get-started/what-is-lotus/) - Lotus offers the full feature set of its capabilities through API.
  - [lotus API Postman sample](https://documenter.getpostman.com/view/4872192/SWLh5mUd?version=latest) - (shows sample wallet calls only)

#### Scalable endpoint hosting

For running a node cluster of load balanced Lotus JSON RPC API endpoints.

- [Filecoin-chart](https://github.com/glifio/filecoin-chart) (k8 cluster) - Helm chart for hosting Lotus Node clients.

#### Filecoin API clients

- [`Filecoin.js`](https://github.com/filecoin-shipyard/filecoin.js) (outdated) -  higher-level JS library for interacting with Lotus via JSON-RPC API.
- [`js-lotus-client`](https://github.com/filecoin-shipyard/js-lotus-client) - lower-level JS wrapper for basic parsing of the Lotus JSON RPC API.
- [`lotus-json-rpc-provider`](https://www.npmjs.com/package/@coinsummer/lotus-jsonrpc-provider)  (outdated) - wraps the Lotus API in TypeScript.

#### Storage provider index API

- [Filrep.io API](https://filrep.io/api) - A suite of RESTFul JSON endpoints to discover the best storage provider to make deals with.
- [Textile storage provider Index](https://blog.textile.io/introducing-the-miner-index/) - API and CLI to find storage providers by price, observed deals, speed from North American nodes.

### Data prep tools

- [CAR files](https://ipld.io/specs/transport/car/) - automatically used on Lotus import for less than 32 and 64 GiB, Filecoin archive format serialized from DAGs, see also [offline deals for large datasets](https://lotus.filecoin.io/tutorials/lotus/large-files/).
- [`go-graphsplit`](https://github.com/filedrive-team/go-graphsplit) - FileDrive chunks a larger single DAG for storage in default Filecoin 32 and 64 GiB sector sizes.
- [IPFS](https://ipfs.tech) - you can use `ipfs add` with an IPFS node then [add the CID from a Filecoin node](https://lotus.filecoin.io/tutorials/lotus/import-data-from-ipfs/).

### Databases using IPFS and Filecoin

- [Tableland](https://tableland.xyz/) - (new) create familiar SQL tables to read and write dynamic NFT metadata or application data for dApps, from Textile
- [OrbitDB](https://orbitdb.org/) - decentralized multi-party database on IPFS with multi-party syncing with topic pubsub and CRDTs. Filecoin integration using Powergate available at [`orbit-db-powergate-io`](https://github.com/filecoin-shipyard/orbit-db-powergate-io).
- [ThreadsDB](https://docs.textile.io/threads/) - decentralized multi-party database for user-siloed data on IPFS, from Textile

### Other developer tools

- [`js-rle`](https://github.com/willscott/js-rle) - RLE+ Spec. Learn about [`rle-bitset-encoding` in the Filecoin Spec](https://spec.filecoin.io/#section-appendix.data_structures.rle-bitset-encoding).
- [Truffle for Filecoin](https://www.trufflesuite.com/docs/filecoin/truffle/quickstart) - building apps to preserve files to IPFS and Filecoin.

## Storage providers

### Storage provider reputation systems

- [Codefi Storage](https://storage.codefi.network/) - view the Filecoin Storage Market, storage provider info, asking price, completed deals.
- [FIL Swan](https://www.filswan.com/) - for offline deals, storage provider info, prices, offline deal acceptance.
- [Filrep.io](https://filrep.io/) - Index of online storage providers and their pricing, ranked by power and reputation score.
- [SpaceGap](https://spacegap.github.io/) - shows storage proof deadlines and sector details for the top 50 storage providers.

### Storage provider tools

- [Bidbot](https://github.com/textileio/bidbot) - A Filecoin Network sidecar to bid in storage deal auctions.
- [Filgas.io](https://fgas.io/) - real-time Filecoin mining gas queries.
- [Lotus Farcaster](https://github.com/s0nik42/lotus-farcaster) - Prometheus, Grafana and Python monitoring dashboard.

### Storage client and miner programs

- [Filecoin storage providers (SPs)](https://sp.filecoin.io/) - Interested in becoming an SP? A boot camp, grants and expert advice is available here!
- [Filecoin Plus Verified Data Program](https://github.com/filecoin-project/filecoin-plus-client-onboarding)
  - incentivizes valuable data stored on Filecoin with a social trust network for verified data
  - Clients can apply to Notaries to receive DataCap and incentivize storage providers at 10x to their quality-adjusted power, increasing probability of block rewards
- [Slingshot Competition](https://slingshot.filecoin.io/) - ended in 2021 and has now become [Filecoin Evergreen](https://evergreen.filecoin.io/)

### Retrieval Market resources (WIP experiments)

The Retrieval Market is in early development; research and development teams are actively exploring improvements.

- [Browser Retrieval Client](https://github.com/filecoin-shipyard/browser-retrieval)
- [Browser Retrieval Client using WASM](https://github.com/jimpick/lotus-retrieve-api-daemon)
- [ChainSafe's Full Node Retrieval Client](https://github.com/ChainSafe/fil-secondary-retrieval-markets)
- [Decentralized Data Delivery Markets - Open Problems and RFCs](https://github.com/protocol/ResNetLab/blob/master/OPEN_PROBLEMS/DECENTRALIZED_DATA_DELIVERY_MARKETS.md)
- [July 2020 Retrieval Markets Workshop](https://www.youtube.com/watch?v=eUcsZ1JS9pM) - list of [Sessions](https://docs.google.com/document/d/17bEHP2CHkQFYYQnl7YpatAOh6kWxjlNgihdc4F66SVM/edit)

## Ecosystem galleries

- [**Community Projects Showcase**](https://github.com/filecoin-project/community/#ecosystem-projects) - updated news about ecosystem projects
- [Filecoin Ecosystem](https://ecosystem.filecoin.io/)

### Hackathons

- [Upcoming Hackathons](https://hackathons.filecoin.io/)
  - Keep a lookout for upcoming hackathons!
  - All winners are eligible for [Next Steps Grants](https://github.com/filecoin-project/devgrants/blob/master/microgrants/microgrants.md) after the Hackathon!

### Grants and accelerators

- [**Filecoin Developer Grants**](https://filecoin.io/grants) - ongoing monthly developer grant program to support open source projects and new [RFPs](https://github.com/filecoin-project/devgrants/tree/master/rfps) on Filecoin, funded by the [Filecoin Foundation](https://fil.org)
