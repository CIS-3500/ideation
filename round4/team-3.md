# ProfitPeak Chrome Extension

## Authors
- Ahmed Abdellah
- Chelsea Pan
- Rayyan Shaik
- Marc Vaz

Usernames: panchel, rashaik, vazmarc, abdellah

---

## Problem Statement
Managing cryptocurrency trades across multiple wallets, chains, and platforms can be daunting, especially for active traders and portfolio managers. The manual tracking of transactions, calculation of profit and loss (PnL), and comprehensive reporting are time-consuming and prone to errors. Moreover, setting up stop-losses and managing risks across various positions pose additional challenges, particularly with the 24/7 trading environment.

---

## Target Audience
**ProfitPeak** is designed for:
- **Active Crypto Traders:** Individuals frequently buying and selling tokens across various platforms and wallets, who seek automatic trade detection to capitalize on market movements.
- **Institutional Portfolio Managers:** Managers of diversified assets across multiple wallets and networks requiring aggregated performance reporting, multi-wallet and cross-chain support, and risk management tools.

---

## Description
**ProfitPeak** aims to provide a streamlined solution for cryptocurrency traders and portfolio managers to monitor and manage their trades and portfolio performance effortlessly. Key features include:
- Automatic Trade Detection
- Profit and Loss Calculation and Reporting
- Risk Management
- Cross-Chain and Multi-Wallet Support
- Customizable User Experience

---

## Selling Points
- **Time-Saving:** Automates trade detection and PnL calculations.
- **Accuracy and Consistency:** Reduces human error in portfolio performance reporting.
- **Risk Mitigation:** Enables custom stop-loss conditions and automated trade executions.
- **Centralized View:** Offers a unified view of trading activities across multiple wallets and chains.
- **Convenience and Accessibility:** Easily accessible as a Chrome extension, without the need for additional software.

---

## User Stories
- Crypto traders want to track all trades and manage assets efficiently.
- Portfolio managers seek to generate aggregated performance reports.
- Traders aim to set up stop-losses for risk management.
- New and experienced traders look for platforms that offer analysis, detailed visualizations, and performance tracking.
- Investors need tools for tax reporting and receiving alerts on trade values.

---

## Notes
Chelsea, Marc, and Rayyan are newcomers to crypto and will need to deepen their understanding, despite grasping the technical aspects.

---

## References & Inspiration
- [MetaMask](https://metamask.io/)

---

## Technical Details

### User Interface
- **Login:** Via WalletConnect for public address user ID.
- **Tabs:** Home (for trade value graphs) and Activity (for past trade details).
- **Features:** Refresh button for latest trade data and market prices.

### API, Libraries, and Frameworks
- **React Frontend** with Vite and component libraries.
- **MySQL + Node.js + Express Backend** for database management.
- **WalletConnect API** for user login and trade data.
- **Etherscan and CryptoCompare APIs** for transaction history and current crypto prices.

### Data Storage
- User account information and trade transactions stored in AWS RDS and potentially cached in-browser for quick access.

---

## Project Management

### Roles
- **Leader:** Ahmed Abdellah (crypto expertise, technical lead)
- **Manager:** Chelsea Pan (project management, backend development)
- **Team Members:** Rayyan Shaik (frontend), Marc Vaz (full-stack)

### Collaboration
Using Notion/Google Docs for documentation and GitHub for code sharing and version control.

---

## Risks and Mitigation
Potential issues with WalletConnect API usage and contingency plans involving manual user ID input for tracking trades.

---

## Milestones and Timeline

- **Week 1:** Tech stack determination, MVP development, and API integration.
- **Week 2:** Backend development, database setup, and extension basics.
- **Week 3:** Continued backend work, frontend initiation with UI components.
- **Week 4:** Backend and frontend integration, finalizing user interaction flows.
