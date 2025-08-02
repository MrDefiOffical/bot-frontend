# Environment Variables Setup

## Required Environment Variables

You need to create a `.env` file in the root directory with the following variables:

### Wallet Configuration
```
PRIVATE_KEY=your_private_key_here
```

### 1inch API Configuration
```
INCH_API_KEY=your_1inch_api_key_here
INCH_API_URL=https://api.1inch.dev
INCH_API_SWAP_URL=https://api.1inch.dev/swap/v6.0
```

### RPC URLs for Different Networks
```
ETH_RPC_URL=https://mainnet.infura.io/v3/your_infura_key
ARBITRUM_RPC_URL=https://arb1.arbitrum.io/rpc
BASE_RPC_URL=https://mainnet.base.org
OPTIMISM_RPC_URL=https://mainnet.optimism.io
```

### Database Configuration
```
MONGODB_URI=your_mongodb_connection_string
```

### Blockchain Explorer API Keys
```
ETHERSCAN_API_KEY=your_etherscan_api_key
ARBISCAN_API_KEY=your_arbiscan_api_key
OPTIMISM_API_KEY=your_optimism_api_key
BASESCAN_API_KEY=your_basescan_api_key
```

### Server Configuration
```
PORT=8000
```

## How to Get These Values

### 1. Private Key
- Export your wallet's private key (be extremely careful with this!)
- Never share or commit this to version control

### 2. 1inch API Key
- Visit https://1inch.dev/
- Sign up and get your API key

### 3. RPC URLs
- **Infura**: Sign up at https://infura.io/ and get your project key
- **Arbitrum**: Use the public RPC or get a dedicated endpoint
- **Base**: Use the public RPC or get a dedicated endpoint  
- **Optimism**: Use the public RPC or get a dedicated endpoint

### 4. MongoDB URI
- Set up a MongoDB database (local or cloud)
- Get the connection string from your MongoDB provider

### 5. Blockchain Explorer API Keys
- **Etherscan**: https://etherscan.io/apis
- **Arbiscan**: https://arbiscan.io/apis
- **Optimism**: https://optimistic.etherscan.io/apis
- **Basescan**: https://basescan.org/apis

## Example .env File

Create a file named `.env` in the root directory with this structure:

```
PRIVATE_KEY=0x1234567890abcdef...
INCH_API_KEY=your_1inch_api_key_here
INCH_API_URL=https://api.1inch.dev
INCH_API_SWAP_URL=https://api.1inch.dev/swap/v6.0
ETH_RPC_URL=https://mainnet.infura.io/v3/your_infura_key
ARBITRUM_RPC_URL=https://arb1.arbitrum.io/rpc
BASE_RPC_URL=https://mainnet.base.org
OPTIMISM_RPC_URL=https://mainnet.optimism.io
MONGODB_URI=mongodb://localhost:27017/mevbot
ETHERSCAN_API_KEY=your_etherscan_api_key
ARBISCAN_API_KEY=your_arbiscan_api_key
OPTIMISM_API_KEY=your_optimism_api_key
BASESCAN_API_KEY=your_basescan_api_key
PORT=8000
```

## Security Notes

⚠️ **IMPORTANT SECURITY WARNINGS:**

1. **Never commit your `.env` file to version control**
2. **Keep your private key secure and never share it**
3. **Use environment-specific API keys for production**
4. **Consider using a hardware wallet for production use**
5. **Test with small amounts first**

The `.env` file is already included in `.gitignore` to prevent accidental commits. 