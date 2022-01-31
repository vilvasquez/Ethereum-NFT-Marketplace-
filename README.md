# `ethereum-boilerplate-NFT-Marketplace`

Este proyecto es una bifurcación de Ethereum Boilerplate y demuestra cómo puede construir su propio NFT Marketplace. Este proyecto, por supuesto, funciona en cualquier cadena de bloques compatible con EVM, como Polygon, Avalanche, Binance Smart Chain y otras cadenas similares.

![Preview](preview.gif)

# ⭐️ `Dejame una Estrella`
este modelo te ayuda a construir dapps de Ethereum más rápido, inicia este proyecto, ¡COmparte el Conocimiento!

# 🚀 Quick Start

📄 Clone or fork `ethereum-nft-marketplace-boilerplate`:
```sh
git clone https://github.com/ethereum-boilerplate/ethereum-nft-marketplace-boilerplate.git
```
💿 Install all dependencies:
```sh
cd ethereum-nft-marketplace-boilerplate
yarn install 
```
✏ Rename `.env.example` to `.env` in the main folder and provide your `appId` and `serverUrl` from Moralis ([How to start Moralis Server](https://docs.moralis.io/moralis-server/getting-started/create-a-moralis-server)) 
Example:
```jsx
REACT_APP_MORALIS_APPLICATION_ID = xxxxxxxxxxxx
REACT_APP_MORALIS_SERVER_URL = https://xxxxxx.grandmoralis.com:2053/server
```

🔎 Locate the MoralisDappProvider in `src/providers/MoralisDappProvider/MoralisDappProvider.js` and paste the deployed marketplace smart contract address and ABI
```jsx
const [contractABI, setContractABI] = useState();
const [marketAddress, setMarketAddress] = useState();
```

🔃 Sync the `MarketItemCreated` event `/src/contracts/marketplaceBoilerplate.sol` contract with your Moralis Server, making the tableName `MarketItems`
```jsx
event MarketItemCreated (
  uint indexed itemId,
  address indexed nftContract,
  uint256 indexed tokenId,
  address seller,
  address owner,
  uint256 price,
  bool sold
);
```


🚴‍♂️ Run your App:
```sh
yarn start
```


