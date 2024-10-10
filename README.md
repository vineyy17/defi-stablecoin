# Decentralized Stablecoin System

A robust, algorithmic stablecoin implementation built on Ethereum.

## Description

This project implements a decentralized, exogenously collateralized stablecoin system using Solidity. The stablecoin is pegged to USD (1 token = $1) and is backed by WETH and WBTC as collateral. The system uses an algorithmic stability mechanism and includes a liquidation system to maintain over-collateralization.

## Key Features

- USD-pegged stablecoin
- Collateralized by ETH and BTC
- No governance or fees
- Algorithmic stability
- Liquidation mechanism

## Smart Contracts

1. `DecentralizedStableCoin.sol`: ERC20 token with minting and burning capabilities.
2. `DSCEngine.sol`: Core logic for collateral management, minting, redeeming, and liquidations.

## Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation)
- Make

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/vineyy17/defi-stablecoin.git
   cd decentralized-stablecoin
   ```

2. Install dependencies:
   ```bash
   make install
   ```

## Usage

### Build

```bash
make build
```

### Test

```bash
make test
```

### Deploy

To deploy on local Anvil chain:
```bash
make deploy
```

To deploy on Sepolia testnet:
```bash
make deploy ARGS="--network sepolia"
```

Note: Make sure to set up your `.env` file with the required environment variables (SEPOLIA_RPC_URL, PRIVATE_KEY, ETHERSCAN_API_KEY) for testnet deployment.

### Other Commands

- Format code: `make format`
- Generate coverage report: `make coverage`
- Take a snapshot: `make snapshot`
- Start local Anvil chain: `make anvil`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.
