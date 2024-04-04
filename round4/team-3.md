# ProfitPeak Chrome Extension

## Authors
Ahmed Abdellah, Chelsea Pan, Rayyan Shaik, Marc Vaz  
Emails: panchel, rashaik, vazmarc, abdellah

---

## Problem Statement
Managing cryptocurrency trades across multiple wallets, chains, and platforms is a daunting task for active traders and portfolio managers. Manually tracking buy and sell transactions, calculating profit and loss (PnL), and generating comprehensive reports is time-consuming and error-prone. Additionally, setting up stop-losses and managing risk across various positions can be challenging, especially when trading opportunities arise at any time of the day or night.

---

## Target Audience
The target audience for ProfitPeak includes active crypto traders and institutional portfolio managers. Active traders are individuals who frequently buy and sell tokens across various platforms and wallets, seeking tools for automatic trade detection to capitalize on market movements. Portfolio managers manage diversified assets across multiple wallets and networks, needing features like aggregated performance reporting, multi-wallet and cross-chain support, and risk-management tools to optimize their strategies. These managers often must report performance to senior-level executives, and generating performance data visualizations are typically a hazard.

---

## Description
The primary goal of the ProfitPeak Chrome extension is to provide a streamlined solution for cryptocurrency traders and portfolio managers to effortlessly monitor and manage their trades, positions, and portfolio performance across multiple wallets and blockchain networks. The extension aims to achieve the following objectives: Automatic Trade Detection, PnL Calculation and Reporting, Risk Management, Cross-Chain and Multi-Wallet Support, and a Customizable User Experience.

---

## Selling Points
- **Time-Saving:** By automating trade detection and PnL calculations, users can save significant time and effort.
- **Accuracy and Consistency:** Automated trade recognition and calculations eliminate the risk of human error, ensuring consistent and accurate reporting.
- **Risk Mitigation:** Custom stop-loss conditions and automated trade executions help users manage risk.
- **Centralized View:** Provides a centralized view of the user's trading activities across multiple wallets and chains.
- **Convenience and Accessibility:** As a Chrome extension, ProfitPeak is easily accessible without additional software or dedicated applications.

---

## User Stories
- As a crypto trader with limited time, I want to be able to track all of my trades.
- As a portfolio manager using multiple chains and providers, I want to create reports for executives on aggregated performance.
- As a trader with a sleep schedule, I want to set up certain stop-losses on risky trades since the market never sleeps.
- As an inexperienced crypto trader, I want a platform that helps me analyze my crypto exchanges and offer detailed visualizations.
- As a crypto trader, I want a centralized platform to quickly see all my past trades and their current worth.
- As a crypto trader looking to improve, I want to analyze the performance of my past trades for strategy improvement.
- As a new trader, I want an easy way to track and visualize my progress.
- As a cryptocurrency enthusiast, I want to manage a wide range of cryptocurrencies and tokens efficiently.
- As a trader, I want the extension to calculate my profit and loss (PnL) for each trade.
- As a crypto investor, I want to easily generate tax reports for my crypto transactions.
- As an avid crypto trader, I want alerts on the values of my trades for informed decision-making.
- As a beginner trader, I want tips and suggestions on when to buy and sell.
- As a crypto trader, I want a tool/platform that aggregates my trades across various (unique) exchanges.
- As a portfolio manager, I want a one-stop shop to see all my transactions for efficient management.
- As a cryptocurrency educator, I want to provide clear reports on transactions to engage my students.

---

## Notes
Chelsea, Marc, and Rayyan don’t have much background knowledge with crypto and will need to do more research. However, they have a general understanding of most of the technical work.

---

## References & Inspiration
https://metamask.io/

---

## Technical Details

### User Interface
When first downloading our extension, it will lead to our website to make the user login with WalletConnect to get their public address user id. This user id will give us access to all their public trade data.

Currently, we are planning to have 2 tabs within the chrome extension. The home tab will display a graph showing the value of your trades over time. The activity tab will display all the past trades of the user in a table, including crypto type, amount, USD value at purchase, purchase date, and current crypto value. We want to include a refresh button to fetch the latest trade data and current market prices of crypto. 

If possible, we aim to add a notification feature that alerts users when the prices of their crypto increase.

### API, Libraries, and Frameworks
- React Frontend
- Vite
- Component libraries?
- MySQL + Node.js + Express? Backend
- WalletConnect API
- https://etherscan.io/
- https://min-api.cryptocompare.com/
- Coingecko free (30 calls/min)

### Data Storage
- Storing user’s account information and etherscan transactions.
- AWS RDS?
- Internal browser caching, localStorage API, and potential server storage for public and non-sensitive data.

---

## Project Management

### Collaboration and Task Allocation
- **Leader:** Ahmed Abdellah
- **Manager:** Chelsea Pan
- **Remaining Team Members:** Rayyan Shaik, Marc Vaz

Roles include backend and frontend development, project management, and across-stack work. Collaboration will use Notion/Google Docs and GitHub.

### Risks and Mitigation
Our biggest risk involves the WalletConnect API for user login. We plan to have users manually input their user ID as a contingency.

---

## Milestones and Timeline
- **Week 1:** Tech stack determination, MVP development.
- **Week 2:** Backend setup, database schema planning.
- **Week 3:** Backend development continuation, frontend start.
- **Week 4:** Backend and frontend integration, final testing.
