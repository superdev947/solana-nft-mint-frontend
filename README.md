# Solana NFT Mint Frontend

A React-based frontend application for minting and managing NFTs on the Solana blockchain. This application provides a complete interface for NFT minting with whitelist/OG list management, multi-stage minting, and NFT gallery viewing.

## 🌟 Features

- **Multi-Stage Minting**: Support for OG list, Whitelist, and Public minting stages
- **Wallet Integration**: Compatible with multiple Solana wallets (Phantom, Slope, Solflare, Torus, Ledger, Sollet)
- **Admin Controls**: Comprehensive admin panel for managing mint stages, pricing, and access lists
- **NFT Gallery**: View and organize your minted NFTs by collection
- **Batch Minting**: Mint multiple NFTs in a single transaction
- **Flexible Pricing**: Set different prices for OG, WL, and Public stages
- **Access Control**: Add/remove wallets from OG and whitelist

## 🛠️ Tech Stack

- **React** 17.0.2 - Frontend framework
- **Solana Web3.js** - Solana blockchain interaction
- **Anchor Framework** - Solana program framework
- **Wallet Adapter** - Multi-wallet support
- **React Bootstrap** - UI components
- **TypeScript** - Type safety
- **@nfteyez/sol-rayz** - NFT data fetching

## 📋 Prerequisites

- Node.js (v14 or higher)
- Yarn package manager
- A Solana wallet (Phantom, Solflare, etc.)
- Basic understanding of Solana blockchain

## 🚀 Getting Started

### Installation

1. Clone the repository:
```bash
git clone https://github.com/superdev947/solana-nft-mint-frontend.git
cd solana-nft-mint-frontend
```

2. Install dependencies:
```bash
yarn install
```

3. The project uses patch-package to apply necessary patches. These will be automatically applied after installation via the `postinstall` script.

### Running the Application

Start the development server:
```bash
yarn start
```

The application will open at [http://localhost:3000](http://localhost:3000)

### Building for Production

Create a production build:
```bash
yarn build
```

The optimized build will be created in the `build` folder.

## 🎮 Usage

### For Users

1. **Connect Wallet**: Click the wallet button in the navigation bar to connect your Solana wallet
2. **Select Network**: Choose between Devnet, Testnet, or Mainnet
3. **Mint NFTs**: 
   - View current stage and price
   - Adjust the mint quantity using +/- buttons
   - Click "Mint" to mint NFTs
4. **View NFTs**: Click "Show NFTs" to view your NFT collection organized by symbol

### For Administrators

The admin panel provides controls for:

#### Initialize Program
- Click "Init" to initialize the minting program

#### Manage Access Lists
- **OG List**: Add/remove wallet addresses for OG access
- **Whitelist**: Add/remove wallet addresses for whitelist access (supports comma-separated addresses)

#### Configure Pricing
- Set different prices for OG, WL, and Public stages
- Prices are in lamports (1 SOL = 1,000,000,000 lamports)
- Click "Update" to apply price changes

#### Configure Mint Limits
- Set maximum mint amounts per stage (OG, WL, Public)
- Click "Update" to apply limit changes

#### Set Base URI
- Configure the base URI for NFT metadata
- Click "Set" to apply

#### Change Mint Stage
- Select from: Disabled, Whitelist, or Public
- Click "Set" to activate the selected stage

## 📁 Project Structure

```
solana-nft-mint-frontend/
├── src/
│   ├── App.js                 # Main application component
│   ├── Main.js                # Wallet provider setup
│   ├── connection.tsx         # Transaction handling utilities
│   ├── utils.js               # Anchor program utilities
│   ├── idl.json              # Program IDL
│   ├── alert/                 # Alert components
│   └── navbar/                # Navigation components
├── public/                    # Static assets
├── patches/                   # Package patches
└── package.json              # Dependencies and scripts
```

## 🔧 Configuration

### Network Configuration

The application supports three networks:
- **Devnet**: For development and testing
- **Testnet**: For staging
- **Mainnet Beta**: For production

Switch networks using the navigation bar dropdown.

### Program Configuration

Update the program ID and connection endpoints in the relevant files:
- Program IDL: `src/idl.json`
- Connection settings: `src/utils.js`

## 📦 Dependencies

Key dependencies include:
- `@solana/web3.js` - Solana blockchain interaction
- `@project-serum/anchor` - Anchor framework client
- `@solana/wallet-adapter-*` - Wallet integration
- `@nfteyez/sol-rayz` - NFT fetching utilities
- `react-bootstrap` - UI components
- `crypto-browserify` - Crypto polyfills for browser

## 🧪 Testing

Run tests with:
```bash
yarn test
```

## 🐛 Troubleshooting

### Common Issues

1. **Wallet Connection Issues**
   - Ensure your wallet extension is installed and unlocked
   - Try refreshing the page
   - Check that you're on the correct network

2. **Transaction Failures**
   - Verify you have enough SOL for transaction fees
   - Check that the mint stage is active
   - Ensure your wallet is on the correct access list (for OG/WL stages)

3. **NFTs Not Showing**
   - Confirm the wallet address is correct
   - Wait a few moments for blockchain confirmation
   - Try clicking "Show NFTs" again

## 🔐 Security Considerations

- Never commit your private keys or seed phrases
- Always verify transaction details before signing
- Use Devnet for testing before deploying to Mainnet
- Implement rate limiting for production deployments
- Validate all user inputs on the smart contract side

## 🚀 Deployment

### Deploying to Vercel

1. Install Vercel CLI:
```bash
yarn global add vercel
```

2. Deploy:
```bash
vercel --prod
```

### Deploying to Netlify

1. Build the project:
```bash
yarn build
```

2. Deploy the `build` folder to Netlify

### Environment Variables

For production deployments, consider using environment variables for:
- RPC endpoints
- Program IDs
- Network selection

## 📝 Scripts

- `yarn start` - Start development server
- `yarn build` - Build for production
- `yarn test` - Run tests
- `yarn eject` - Eject from Create React App (irreversible)
- `yarn postinstall` - Apply patches automatically

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🔗 Links

- [Solana Documentation](https://docs.solana.com/)
- [Anchor Framework](https://www.anchor-lang.com/)
- [Wallet Adapter](https://github.com/solana-labs/wallet-adapter)
- [Create React App Documentation](https://facebook.github.io/create-react-app/docs/getting-started)

## 🙏 Acknowledgments

- Solana Foundation
- Metaplex Protocol
- Anchor Framework Team
- NFTEyez for the sol-rayz library

---

**Note**: This application is currently configured for Devnet. Before deploying to Mainnet, ensure all configurations are properly updated and thoroughly tested.

## 📸 Screenshots

### Main Interface
The main interface shows the current mint stage, price, and mint controls.

### NFT Gallery
View your minted NFTs organized by collection with metadata.

### Admin Panel
Comprehensive controls for managing the minting process.
