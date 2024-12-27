# Aptos NFT Marketplace

## Overview
This frontend application is built to interact with an NFT marketplace smart contract deployed on the Aptos blockchain. The marketplace supports minting, listing, buying, selling, and burning NFTs, with features for categories, tags, and rarity levels.

## Features
- **Mint NFTs:** Create unique NFTs with metadata like name, description, URI, rarity, category, and tags.
- **List NFTs for Sale:** Set a price and list your NFTs for sale.
- **Buy NFTs:** Purchase listed NFTs, with a 2% marketplace fee and 5% creator royalty.
- **View NFTs:** Retrieve details of individual NFTs, all NFTs for a specific owner, or NFTs for sale.
- **Burn NFTs:** Mark an NFT as permanently burned to exclude it from the marketplace.
- **Filter by Rarity:** Fetch NFTs by rarity level.

## Frontend Implementation
The frontend is developed using modern web technologies (React.js). It connects to the smart contract using the Aptos SDK and integrates with the blockchain wallet.

### Prerequisites
1. **Node.js and npm:** Ensure Node.js and npm are installed.
2. **Aptos Wallet:** Set up and connect an Aptos wallet for user transactions.
3. **Aptos SDK:** Install the SDK for interacting with the blockchain.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/0xiammatrixx/apt4bounty.git
   cd aptos4-q2
   ```
2. Install dependencies:
   ```bash
   npm i @aptos-labs/wallet-adapter-react @aptos-labs/wallet-adapter-ant-design petra-plugin-wallet-adapter --legacy-peer-deps
   ```
   
### Usage
1. Start the development server:
   ```bash
   npm start
   ```
2. Open the app in your browser at `http://localhost:3000`.

### Key Components
#### **1. Minting NFTs**
- Users can mint NFTs by filling out a form with the required metadata.
- Frontend calls the `mint_nft` function on the contract.

#### **2. Listing NFTs**
- NFT owners can list their NFTs for sale.
- Frontend interacts with the `list_for_sale` function.

#### **3. Purchasing NFTs**
- Users can buy NFTs listed for sale.
- Frontend interacts with the `purchase_nft` function, calculates fees, and updates ownership.

#### **4. Viewing NFTs**
- Fetch NFTs by owner, rarity, or sale status using functions like:
  - `get_all_nfts_for_owner`
  - `get_all_nfts_for_sale`
  - `get_nfts_by_rarity`

#### **5. Burning NFTs**
- Allows users to mark NFTs as burned, making them untradeable and invisible.

### Wallet Integration
- The app supports Aptos wallets for signing transactions.
- Wallet connection is required for all blockchain interactions.

### Advanced Features
- **Rarity Filters:** Display NFTs categorized by rarity (e.g., common, rare, epic).
- **Search and Pagination:** Efficiently fetch NFTs with limit and offset for large collections.
- **Royalties:** Automatically calculate and distribute royalties to creators on purchase.
- **Tags:** Introduction of categories and tags for better NFT discovery.


### Contributing
Contributions are welcome! Fork the repository and submit a pull request with your changes.

### License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

If you encounter any issues, feel free to open an issue in the repository or contact the maintainer.
