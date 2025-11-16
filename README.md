# 🚀 AeroSwap

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Vue](https://img.shields.io/badge/Vue-3.4+-4FC08D?logo=vue.js)
![Vite](https://img.shields.io/badge/Vite-5.2+-646CFF?logo=vite)

**A modern decentralized exchange (DEX) built on Dolphinet**

[Features](#-features) • [Quick Start](#-quick-start) • [Documentation](#-documentation) • [Contributing](#-contributing)

</div>

---

## 📖 About

AeroSwap is a decentralized exchange protocol built on the Dolphinet network, providing users with a seamless token swapping experience. The platform features an intuitive interface, multi-language support, and robust security measures for DeFi transactions.

### ✨ Key Features

- 🔄 **Token Swapping**: Swap tokens directly on Dolphinet with minimal slippage
- 💼 **Wallet Integration**: Connect with popular wallets via Wagmi
- 🌍 **Multi-language Support**: Full support for Chinese and English
- ⚙️ **Customizable Slippage**: Adjustable slippage tolerance settings
- 🎨 **Modern UI**: Clean, responsive design with smooth animations
- 🔒 **Secure Transactions**: Built with security best practices
- 📱 **Responsive Design**: Optimized for desktop and mobile devices
- 🌐 **Network Support**: Compatible with Dolphinet Mainnet and Testnet

## 🛠️ Tech Stack

### Core Technologies
- **Vue 3** - Progressive JavaScript framework
- **Vite** - Next-generation frontend build tool
- **TypeScript** - Type-safe JavaScript
- **Pinia** - State management
- **Vue Router** - Client-side routing

### Blockchain Integration
- **Wagmi** - React Hooks for Ethereum (Vue port)
- **Ethers.js** - Ethereum JavaScript library
- **Viem** - TypeScript Ethereum library
- **Uniswap V2 SDK** - DEX protocol integration

### UI & Styling
- **Element Plus** - Vue 3 component library
- **SCSS** - CSS preprocessor
- **Animate.css** - Animation library

### Internationalization
- **Vue I18n** - Internationalization plugin

## 📦 Installation

### Prerequisites

- **Node.js** >= 18.0.0
- **npm** >= 9.0.0 or **pnpm** >= 8.0.0

### Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd swap-app
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   pnpm install
   ```

3. **Configure environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   VITE_CHAIN_ID=your_chain_id
   VITE_RPC_URL=your_rpc_url
   ```

## 🚀 Quick Start

### Development

Start the development server:

```bash
npm run dev
```

The application will be available at `http://localhost:3000`

### Build

Build for production:

```bash
npm run build
```

The built files will be in the `dist` directory.

### Preview

Preview the production build:

```bash
npm run preview
```

### Lint

Run the linter:

```bash
npm run lint
```

## 📁 Project Structure

```
swap-app/
├── src/
│   ├── assets/          # Static assets (images, fonts, etc.)
│   ├── components/      # Vue components
│   │   ├── navBar.vue   # Navigation bar component
│   │   └── popup.vue    # Popup component
│   ├── config/          # Configuration files
│   ├── languages/       # Internationalization files
│   │   └── locales/
│   │       ├── en_US.js # English translations
│   │       └── zh-CN.js # Chinese translations
│   ├── router/          # Vue Router configuration
│   ├── stores/          # Pinia stores
│   ├── styles/          # Global styles
│   │   ├── fonts.scss   # Font definitions
│   │   ├── global.scss  # Global styles
│   │   └── themes.scss  # Theme variables
│   ├── utils/           # Utility functions
│   ├── views/           # Page components
│   │   └── swap/
│   │       ├── index.vue      # Main swap page
│   │       ├── doSwap.js       # Swap execution logic
│   │       ├── uniswapQuote.js # Quote estimation
│   │       ├── tokenSelect.vue # Token selection modal
│   │       └── SlippageModal.vue # Slippage settings
│   ├── App.vue          # Root component
│   ├── main.ts          # Application entry point
│   └── wagmi.ts         # Wagmi configuration
├── public/              # Public assets
├── dist/                # Build output
├── index.html           # HTML template
├── vite.config.ts       # Vite configuration
├── tsconfig.json        # TypeScript configuration
└── package.json         # Project dependencies
```

## 🎯 Features

### Token Swapping

- Swap between native DOL tokens and Dolphinet tokens
- Real-time price quotes
- Minimum received amount calculation
- Transaction status tracking

### Wallet Connection

- Support for multiple wallet providers
- Account balance display
- Transaction history
- Network switching

### User Interface

- **Light Theme**: Modern, clean design
- **Responsive Layout**: Works on all screen sizes
- **Smooth Animations**: Subtle background animations
- **Accessibility**: Keyboard navigation support

### Internationalization

- **English**: Full English language support
- **Chinese (Simplified)**: Complete Chinese translation
- **Language Switching**: Easy language toggle in navigation

## 🔧 Configuration

### Network Configuration

Configure supported networks in `src/config/`:

```typescript
export const networks = {
  mainnet: {
    chainId: 1,
    rpcUrl: 'https://mainnet.dolphinet.com',
    // ...
  },
  testnet: {
    chainId: 2,
    rpcUrl: 'https://testnet.dolphinet.com',
    // ...
  }
}
```

### Theme Customization

Modify theme variables in `src/styles/themes.scss`:

```scss
:root {
  --bg-color: #ffffff;
  --text-color: #1a1a1a;
  --el-menu-active-color: #00CE7A;
  // ...
}
```

## 📚 Documentation

### Development Guide

1. **Adding a New Token**
   - Add token information to the token list
   - Configure token metadata (symbol, decimals, address)

2. **Customizing Styles**
   - Modify SCSS variables in `themes.scss`
   - Update component styles in respective `.vue` files

3. **Adding Translations**
   - Add new keys to `src/languages/locales/en_US.js`
   - Add corresponding translations to `zh-CN.js`

### API Reference

- **Swap Function**: `doSwaps()` in `src/views/swap/doSwap.js`
- **Quote Estimation**: `estimateQuotes()` in `src/views/swap/uniswapQuote.js`

## 🚢 Deployment

### Docker Deployment

Build and run with Docker:

```bash
docker build -t aeroswap .
docker run -p 3000:3000 aeroswap
```

### Static Hosting

The `dist` folder contains static files that can be deployed to:

- **Vercel**: `vercel deploy`
- **Netlify**: Drag and drop `dist` folder
- **GitHub Pages**: Configure in repository settings
- **Nginx**: Copy `dist` contents to web root

### Environment Variables

Set the following environment variables for production:

```env
VITE_CHAIN_ID=production_chain_id
VITE_RPC_URL=production_rpc_url
VITE_ROUTER_ADDRESS=router_contract_address
```

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style

- Follow Vue 3 Composition API best practices
- Use TypeScript for type safety
- Write meaningful commit messages
- Add comments for complex logic

## 🐛 Known Issues

- Some animations may be disabled on low-end devices
- Large token lists may cause performance issues (consider pagination)

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Uniswap](https://uniswap.org/) for the DEX protocol
- [Wagmi](https://wagmi.sh/) for wallet integration
- [Element Plus](https://element-plus.org/) for UI components
- [Vue.js](https://vuejs.org/) community

## 📞 Support

For support, please open an issue in the GitHub repository or contact the development team.

---

<div align="center">

**Made with ❤️ for the Dolphinet community**

[Report Bug](https://github.com/your-repo/issues) • [Request Feature](https://github.com/your-repo/issues) • [Documentation](https://docs.aeroswap.com)

</div>
