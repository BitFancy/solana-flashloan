# Composable Solana Flash Loan 🚀

Welcome to the **Composable Solana Flash Loan** repository! This project implements a modern, composable flash loan mechanism on the Solana blockchain, leveraging Solana's unique features like **instruction introspection** and **atomic transactions**. Unlike traditional EVM-based flash loans, this implementation is designed to be more flexible, efficient, and secure, making it ideal for DeFi applications such as arbitrage, liquidations, and more.

---

## 🌟 Key Features

- **Composable Flash Loans**: Use Solana's instruction introspection to create atomic, composable flash loan transactions.
- **Reward Fee System**: Configure dynamic reward fees for liquidity providers.
- **Discount Vouchers**: Incentivize timely repayments with discount vouchers.
- **Atomic Execution**: All operations within a transaction either succeed or fail together, ensuring safety and reliability.
- **Modern Solana Tooling**: Built with **Anchor Framework** and **Rust** for maximum performance and security.

---

## 🛠️ Installation

To get started, ensure you have the following tools installed:

1. **Rust**: Install via [rustup](https://www.rust-lang.org/tools/install).
   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

2. **Solana CLI**: Install the Solana CLI (version 1.9.14 or later) from the [official documentation](https://docs.solana.com/cli/install-solana-cli-tools).
   ```bash
   sh -c "$(curl -sSfL https://release.solana.com/v1.9.14/install)"
   ```

3. **Anchor Framework**: Install Anchor (version 0.23 or later) using the [Anchor installation guide](https://book.anchor-lang.com/chapter_2/installation.html).
   ```bash
   cargo install --git https://github.com/project-serum/anchor anchor-cli --locked
   ```

4. **Node.js**: Install Node.js (version 17.4.0 or later) using [nvm](https://github.com/nvm-sh/nvm).
   ```bash
   nvm install 17.4.0
   ```

5. **Yarn**: Install Yarn for dependency management.
   ```bash
   npm install -g yarn
   ```

---

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/bitfancy/solana-flashloan.git
cd solana-flashloan
```

### 2. Install Dependencies
```bash
yarn install
```

### 3. Build the Smart Contract
```bash
anchor build
```

### 4. Run Tests
```bash
anchor test
```

---

## 🧠 How It Works

### Overview
This flash loan implementation leverages Solana's **instruction introspection** to inspect and validate the instructions within a transaction. This allows for atomic execution of complex operations, ensuring that all parts of a transaction succeed or fail together.

### Key Concepts
1. **Instruction Introspection**: Solana programs can inspect the instructions within a transaction, enabling validation of the flash loan repayment logic.
2. **Atomic Transactions**: All instructions in a Solana transaction are executed atomically. If any instruction fails, the entire transaction is reverted.
3. **Reward Fees**: Liquidity providers earn a reward fee for facilitating flash loans.
4. **Discount Vouchers**: Users can use discount vouchers to reduce the repayment amount, incentivizing timely repayments.

### Workflow
1. **Borrow Funds**: A user initiates a flash loan by specifying the amount to borrow and the operations to perform.
2. **Execute Operations**: The user includes the necessary instructions (e.g., arbitrage, liquidation) within the same transaction.
3. **Repay Loan**: The user repays the borrowed amount plus fees. If a discount voucher is used, the repayment amount is reduced.
4. **Validation**: The flash loan program validates the transaction to ensure the loan is repaid and all operations are executed correctly.

---

## 🛠️ Usage Guide

### 1. Set Up the Environment
1. Start a local Solana validator:
   ```bash
   solana-test-validator
   ```

2. Configure the Solana CLI to use the local validator:
   ```bash
   solana config set --url localhost
   ```

3. Deploy the program:
   ```bash
   anchor deploy
   ```

### 2. Interact with the Flash Loan Program
- **Initialize the Program**: Use the `initialize` instruction to set up the program with reward fees and discount voucher settings.
- **Request a Flash Loan**: Use the `request_flash_loan` instruction to borrow funds and specify the operations to perform.
- **Repay the Loan**: Use the `repay_flash_loan` instruction to repay the borrowed amount plus fees.
- **Use Discount Vouchers**: Include a discount voucher in the repayment transaction to reduce the repayment amount.

---

## 📂 Project Structure

```
composable-solana-flash-loan/
├── programs/              # Solana program (smart contract) code
│   └── flash-loan/        # Flash loan program logic
├── tests/                 # Integration and unit tests
├── migrations/            # Deployment scripts
├── app/                   # Frontend or client application (if applicable)
├── Anchor.toml            # Anchor configuration file
├── Cargo.toml             # Rust dependencies
└── README.md              # This file
```

---

## 🧪 Testing

Run the test suite to ensure everything works as expected:
```bash
anchor test
```

---

## 💬 Contact

For questions, feedback, or collaboration opportunities, feel free to reach out:

- **Email**: bitbanana717@gmail.com
- **Telegram**: Follow [@bitfancy](https://t.me/bitfancy)
- **Discord**: Send DM [bitbanana717](@bitbanana717)

---

## 🙌 Contributing

We welcome contributions! If you'd like to contribute, please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature or bugfix.
3. Submit a pull request with a detailed description of your changes.

---

## 🌟 Show Your Support

If you find this project useful, please give it a ⭐️ on GitHub! Your support helps us improve and grow the project.

---

Built with ❤️ by [bitfancy]. Happy coding! 🚀