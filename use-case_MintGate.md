# MintGate
**Overview of MintGate & Discovery of Rarible Protocol:**

MintGate was born from the first Gitcoin Kernel launchpad.

MintGate realized that many social tokens were being minted at the time, but they had limited utility. As a result, they created a general purpose solution to add utility to any token; access through ownership, or token gating exclusive videos, audio, or documents so only token holders can access it.

As NFTs grew in popularity, MintGate recognized that most NFTs hold subjective value but no instrinsic, objective value. In using the same technology applied to social tokens, they are able to add utility, or functional value, to any NFT by allowing creators to gate content only accessible by holders of their NFTs.

Creators who continually produce high quality content can expect access to that content to increase in value as early buyers are incentivized to promote them to see their NFTs appreciate in value, thus growing the creators branding awareness. 

As MintGate started researching NFT royalties and building out a marketplace to trade NFTs with unlockable content, they learned that Rarible was developing an open protocol and DAO that provided all the technology necessary to bootstrap this. Instead of reinventing the wheel, MintGate decided to join the DAO and start building their marketplace on the protocol to provide the best experience for their growing community of creators and influencers. 

**How MintGate would have changed things knowing what they know now:**

One thing Mintgate would have done differently based on experience is to prioritize the Rarible marketplace order creation features sooner instead of focusing on lazy minting alone. 

Also, they hope Rarible will be able to complete an SDK alternative to the APIs because they fail from time to time, causing confusion for users and bugs when there is no sale order or lazy mint created. Using a SDK would hopefully prove more reliable.  

**Step by step instructions for how MintGate started building on Rarible protocol:**

*Always test on testnet before deploying to mainnet. Ropsten recommended for using Rarible APIs.*

1. Fork Rarible Protocol: https://github.com/rarible/protocol-contracts (Best to explore and get familiar)
2. Identify which NFT token type you will be using, 721 or 1155, and make any modifications necessary in the tokens folder: https://github.com/rarible/protocol-contracts/tree/master/tokens
3. Update the migrations files to pass in whatever parameters you want for the contract you plan to deploy: https://github.com/rarible/protocol-contracts/tree/master/tokens/migrations
      **Note:** Only migration files 1-4 are necessary for initial deployment, and only #2 for 721 and #3 for 1155 if you don't want to deploy contracts for both
4. Take note of the addresses for the contracts. These are upgradeable contracts, so you will be directing calls to the proxy address. 
5. Test some functions like `name()` or `symbol()` in your terminal to ensure it's working
6. Start using Rarible's APIs for lazy minting and order creation to build out your marketplace: https://api-reference.rarible.com/#operation/upsertOrder

APIs for MintGate for token gating are also available. 

Full documentation and instructions can be found here:
[MintGate Docs](https://mintgate.gitbook.io/mintgate-docs/)

Currently, the MintGate team is working on API wrappers that tie-in to the Rarible Protocol endpoints and future projections are to create a subgraph to reach full decentralization.
