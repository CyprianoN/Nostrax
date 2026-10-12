# Nostrax

Nostrax is a decentralized prediction market platform that enables users to create prediction markets, trade positions, and participate in market resolution through smart contracts. The platform combines on-chain market operations with a reputation system to support transparent, trust-minimized prediction markets.

## Features

- **Prediction Markets:** Create and participate in binary and multi-outcome prediction markets.
- **Market Trading:** Buy and sell market positions.
- **On-Chain Transactions:** Interact with prediction markets through blockchain smart contracts.
- **ETH and ERC-20 Support:** Participate in markets using supported digital assets.
- **Peer-to-Peer Position Trading:** Trade positions with other participants without a platform trading fee.
- **Market Resolution:** Resolve markets through an arbitrator-based resolution mechanism.
- **Reputation System:** Track participant reputation to support accountability across the platform.
- **Winnings Distribution:** Automatically distribute winnings through smart contracts, with a 2% fee applied to winnings.
- **Wallet Integration:** Connect compatible Web3 wallets.
- **Responsive Interface:** Access market information and trading features through a responsive web interface.

## Tech Stack

### Smart Contracts

- **Solidity:** Smart contract development.
- **Hardhat:** Smart contract development, compilation, testing, and deployment.
- **OpenZeppelin:** Reusable smart contract components and security utilities.
- **Ethereum:** Blockchain infrastructure for market operations.

### Frontend

- **Next.js 16:** React framework for the web application.
- **React 19:** User interface development.
- **TypeScript:** Static typing and maintainable application code.
- **Tailwind CSS 4:** Utility-first styling.
- **shadcn/ui:** Reusable interface components.
- **Radix UI:** Accessible, unstyled UI primitives.
- **Wagmi:** React hooks for Ethereum interactions.
- **Viem:** Type-safe Ethereum clients and utilities.
- **RainbowKit:** Wallet connection interface.
- **TanStack Query:** Server-state management, caching, and asynchronous data handling.
- **React Hook Form:** Form state management.
- **Zod:** Schema validation.
- **Recharts:** Data visualization.
- **Lucide React:** Interface icons.
- **Sonner:** Toast notifications.
- **next-themes:** Theme management.
- **date-fns:** Date utilities.

### Testing Tools

The following tools are candidates for the testing setup and should be installed and configured before being treated as part of the project's existing toolchain:

- **Vitest:** Unit and component test runner.
- **React Testing Library:** Component behavior testing.
- **Playwright:** End-to-end browser testing.
- **Mock Service Worker (MSW):** Mocking API requests during tests.

## Network

The application targets the Ethereum Sepolia test network.

| Property | Value |
|---|---|
| Network | Ethereum Sepolia |
| Chain ID | `11155111` |
| Environment | Testnet |

Ensure that your connected wallet is configured for Sepolia and has sufficient test ETH for applicable transactions.

## Getting Started

### Prerequisites

Before running the application, ensure you have:

- Node.js installed in a version compatible with the project's Next.js version.
- npm installed.
- Git installed.
- A compatible Web3 wallet.
- Access to the Ethereum Sepolia test network.
- A WalletConnect project ID if required by the wallet connection configuration.

### Installation

Clone the repository:

```bash
git clone https://github.com/CyprianoN/Nostrax.git
```

Navigate into the project directory:

```bash
cd Nostrax
```

Install dependencies:

```bash
npm install
```

Configure the required environment variables as described in the Environment Variables section.

## Environment Variables

Create a `.env.local` file in the project root and configure the environment variables required by the application.

```env
NEXT_PUBLIC_WALLETCONNECT_PROJECT_ID=
NEXT_PUBLIC_PREDICTION_MARKET_ADDRESS=
NEXT_PUBLIC_REPUTATION_SYSTEM_ADDRESS=
NEXT_PUBLIC_MOCK_USDC_ADDRESS=
```

Replace the empty values with the appropriate project ID and deployed contract addresses.

The variable names above must match the names referenced in the application's configuration and source code. Update them if the application uses different names.

**Important:** Variables prefixed with `NEXT_PUBLIC_` are exposed to the browser. Never store private keys, seed phrases, API secrets, or other sensitive credentials in these variables.

## Running the Application

### Development Server

Start the development server:

```bash
npm run dev
```

The application will be available at:

```text
http://localhost:3000
```

The development server uses Next.js with Turbopack.

### Production Build

Create a production build:

```bash
npm run build
```

Start the production server:

```bash
npm run start
```

Run the production server after successfully generating the build.

### Linting

Run ESLint:

```bash
npm run lint
```

Resolve reported linting issues before submitting changes.

## Available Scripts

| Command | Description |
|---|---|
| `npm run dev` | Starts the development server with Turbopack. |
| `npm run build` | Creates a production build with Turbopack. |
| `npm run start` | Starts the production server. |
| `npm run lint` | Runs ESLint. |

## Testing

Testing should cover the frontend, smart contracts, and critical market workflows.

### Frontend Testing

Recommended coverage includes:

- Component rendering and user interactions.
- Form validation and error handling.
- Wallet connection and network selection.
- Market data loading and empty states.
- Transaction pending, success, and failure states.
- Position creation, trading, and market resolution interfaces.
- Reputation display and updates.

### Smart Contract  Testing

Smart contract tests should cover:

- Market creation and configuration.
- Market participation and position trading.
- Input validation and access control.
- Market resolution and settlement.
- Winnings calculation and distribution.
- Application of the 2% fee on winnings.
- Reputation updates.
- Invalid transactions and unauthorized actions.
- Reentrancy protection and other relevant security scenarios.

### End-to-End Testing

End-to-end tests should verify complete user workflows, including connecting a wallet, selecting a market, participating in a market, trading a position, and reviewing resolved market outcomes.

The testing tools listed in the Tech Stack section are recommendations unless they are already installed and configured in the repository.

## Documentation

The `docs/` directory contains the project's technical documentation.

| Document | Description |
|---|---|
| [Project Overview](./docs/01-overview.md) | Introduction to Nostrax, its purpose, and its architecture. |
| [Smart Contracts](./docs/02-smart-contracts.md) | Smart contract architecture and implementation details. |
| [Market Lifecycle](./docs/03-market-lifecycle.md) | Market creation, operation, resolution, and settlement. |
| [Position Trading](./docs/04-position-trading.md) | Position trading concepts and workflows. |
| [Reputation System](./docs/05-reputation-system.md) | Reputation mechanics and related functionality. |
| [Frontend Architecture](./docs/06-frontend%20architecture.md) | Frontend structure and architectural decisions. |
| [Hooks and Data](./docs/07-hooks-and-data.md) | Application hooks and data management. |
| [UI Components](./docs/08-ui-components.md) | Interface components and their organization. |
| [Development Setup](./docs/09-development-setup.md) | Development environment configuration and setup instructions. |
| [Deployment](./docs/10-deployment.ind) | Deployment documentation. |
| [User Flows](./docs/11-user-flows.md) | User journeys and application workflows. |
| [API Reference](./docs/12-api-reference.md) | API and integration reference. |
| [Testing Guide](./docs/TESTING.md) | Testing guidance and procedures. |

## Project Status

Nostrax is maintained in a proprietary repository. Access to the source code and project documentation is managed through the repository's configured permissions.