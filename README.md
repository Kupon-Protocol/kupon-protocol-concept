# Kupon Protocol

Kupon Protocol allows users to create **NFTs** that serve **as coupons** or **vouchers**. 

**A few use cases:**

- A company can create a limited supply NFT that represents a 20% discount for a specific product.
- An influencer can offer paid NFTs that allow each holder to schedule a 30-min video chat with the influencer.
- A tutor can issue paid NFTs that represent tutoring time slots.

### Proof-of-concept

A minimum viable version (with only the core features) would include the following:

- A factory smart contract, through which a user can generate an ERC-721 contract
- The ERC-721 contract has the following features:
  - **Name/title**: e.g. A 20% discount on product XYZ.
  - **Price for minting an NFT**: coupons should be free to mint, but vouchers usually have a certain price.
  - **Max supply**: how many tokens can be minted
  - **Marking token as "used"**: Once used, the token should be marked as such so that it cannot be used again.

### Additional features

Later on, additional features can be added:

- Token payments can be withheld within an NFT until the NFT is "used" (i.e. the NFT holder has received the service/product that the NFT has offered).
- **Dispute resolution system**: Both NFT issuer and holder should be allowed to raise a dispute (something like Kleros could be integrated to resolve disputes).
- **Expiration date**: An issuer could set an expiration date for tokens. This can either be a relative date (e.g. 30 days after minting) or an absolute date (e.g. until the end of 2024). In addition, the issuer could have the possibility to extend the expiration date.
- **Refunds**: If a token buyer changes their mind, they could be reimbursed (if NFT allows that).
- **Metadata**: Metadata could include NFT description, image, terms & conditions, etc.
- **Perpetual NFT offerings**: Instead of having a max absolute supply, the NFT contract could have a max active (or unused) supply. If the max supply is hit, the only way to mint another token is to wait until one of the existing tokens is marked as "used".
- A percentage of each paid NFT mint could potentially go to Kupon DAO. The DAO could decide on what the percentage amount should be.
  - The minting fee could be split between the Kupon DAO and the referrer (the front-end maintainer).
- **POAPs:** Potential integration with poap.xyz

### User interfaces / front-ends

The Kupon Protocol can be used by multiple front-ends for various use cases. For example, a web3 website that offers users discount coupons, or a mobile app that allows you to schedule a call with your favorite celebrity.

Front-ends should also offer the way for an NFT holder to prove they really own the NFT in question. An NFT issuer could ask a holder to sign a certain message with their address through the front-end.

### TODO

In order to prepare a proof-of-concept, the following needs to be done:

- Protocol specs (architecture, variables, functions)
- [Smart contracts (Solidity, Hardhat)](https://github.com/Kupon-Protocol/kupon-protocol-contracts)
- Front-end design (preferably Figma)
- Web3 app (preferably Vue, ethers.js)

### Discussion

What do you think about Kupon Protocol? Please share your thoughts in this discussion: https://github.com/Kupon-Protocol/kupon-protocol-concept/discussions/1 
