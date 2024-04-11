# ProfitPeak Chrome Extension

## Authors
Ahmed Abdellah, Chelsea Pan, Rayyan Shaik, Marc Vaz  
Emails: panchel, rashaik, vazmarc, abdellah

---

## Problem Statement
Managing cryptocurrency trades across multiple wallets, chains, and platforms can be a daunting task, especially for active traders and portfolio managers. Manually tracking buy and sell transactions, calculating profit and loss (PnL), and generating comprehensive reports can be time-consuming and error-prone. Additionally, setting up stop-losses and managing risk across various positions can be challenging, particularly when trading opportunities arise at any time of the day or night.

---

## Target Audience
The target audience for ProfitPeak includes active crypto traders and institutional portfolio managers. Active traders are individuals who frequently buy and sell tokens across various platforms and wallets, seeking tools for automatic trade detection to capitalize on market movements. On the other hand, portfolio managers manage diversified assets across multiple wallets and networks. They need features like aggregated performance reporting, multi-wallet and cross-chain support, and risk-management tools to optimize their strategies. These managers often must report performance to senior level executives and generating performance data visualizations are typically a hazard. 

---

## Description
The primary goal of the ProfitPeak Chrome extension is to provide a streamlined solution for cryptocurrency traders and portfolio managers to effortlessly monitor and manage their trades, positions, and portfolio performance across multiple wallets and blockchain networks. The extension aims to achieve the following objectives:Automatic Trade Detection, PnL Calculation and Reporting, Risk Management, Cross-Chain and Multi-Wallet Support, and a Customizable User Experience

---

## Selling Points
- **Time-Saving:** By automating trade detection and PnL calculations, users can save significant time and effort that would otherwise be spent manually tracking and consolidating data from multiple sources.
- **Accuracy and Consistency:** With automated trade recognition and calculations, the extension eliminates the risk of human error and ensures consistent and accurate reporting of portfolio performance.
- **Risk Mitigation:** The ability to set custom stop-loss conditions and automate trade executions helps users effectively manage risk and protect their investments, even during periods of market volatility or when unable to actively monitor positions.
- **Centralized View:** The extension provides a centralized view of the user's trading activities across multiple wallets and chains, enabling better decision-making and portfolio management.
- **Convenience and Accessibility:** As a Chrome extension, ProfitPeak offers a convenient and easily accessible solution, eliminating the need for additional software installations or dedicated applications running in the background.

---

## User Stories
- As a crypto trader with limited time, I want to be able to track all of my trades.
- As a portfolio manager using multiple chains and providers, I want to be able to create reports for executives on aggregated performance.
- As a trader with a sleep schedule, I want to set up certain stop-losses on risky trades since the market never sleeps.
- As an inexperienced crypto trader, I want a platform that helps me analyze my crypto exchanges and offer detailed visualizations to help me understand my trading efficiency.
- As a crypto trader, I want a centralized platform to quickly see all my past trades and what they are worth now so that I can track my progress.
- As a crypto trader looking to improve, I want to analyze the performance of my past trades for strategy improvement.
- As a new trader, I want an easy way to track and visualize my progress so that I can keep learning.
- As a cryptocurrency enthusiast, I want to be able to manage a wide range of cryptocurrencies and tokens, so that I can manage all my assets efficiently.
- As a trader, I want the extension to calculate my profit and loss (PnL) for each trade, so that I can accurately evaluate the success of my trading strategies.
- As a crypto investor, I want to easily generate tax reports for my crypto transactions so that I can comply with regulations without hassle.
- As an avid crypto trader, I want alerts on the values of my trades so that I can make informed decisions about my crypto investments.
- As a beginner trader, I want tips and suggestions on when to buy and sell so that I can keep learning to become a better trader.
- As a crypto trader, I want a tool/platform that aggregates my trades across various (unique) exchanges.
- As a portfolio manager, I want a one stop shop to see all my transactions so that I can quickly manage them all at once. 
- As a cryptocurrency educator, I want to provide clear reports on transactions so that I can engage my students and help them develop a deeper understanding of blockchain technology and trading strategies.
---

## Notes
Chelsea, Marc, and Rayyan don’t have much background knowledge with crypto, so they will need to do more research on the topic. However, they have a general understanding of most of the technical work.

---

## References & Inspiration
https://metamask.io/

---

## Technical Details

### User Interface
When first downloading our extension, it will lead to our website to make the user login with WalletConnect to get their public address user id. This user id will give us access to all their public trade data.

Currently, we are planning to have 2 tabs within the chrome extension. The home tab will display a graph showing the value of your trades over time. The activity tab will display all the past trades of the user in a table. That would include what type of crypto they bought, the amount bought, the value it was bought at in USD, the date bought, and the current value of the crypto. Within the extension, we want to include a refresh button to fetch latest trade data and current market prices of crypto. 

If we’re able to get to it, we want to add a notification feature that alerts users when prices of their crypto increase. 

### API, Libraries, and Frameworks
- React Frontend
- Vite 
- Component libraries?
- MySQL + Node.js + Express? Backend
- WalletConnect API 
- Have user log in to their account and get their user id from the log in. Use this info to get trade transactions
- https://etherscan.io/
- Viewing wallet transaction history
- API Available: https://etherscan.io/apis
- (Would require our own backend / server to restrict usage)
- https://min-api.cryptocompare.com/
- API to get current prices of crypto currencies 
- Coingecko free (30 calls / min)


### Data Storage
- Storing user’s account information and etherscan transactions.
- AWS RDS?
- Storing etherscan transitions potentially in the browser caching
- Internal browser caching, localStorage API (public and non sensitive data), and potential server storage for public and non-sensitive data.
- Data can also be stored on a (potential?) server
---

## Project Management

### Collaboration and Task Allocation
- **Leader:** Ahmed Abdellah
- **Manager:** Chelsea Pan
- **Remaining Team Members:** Rayyan Shaik, Marc Vaz

Ahmed Abdellah- has background knowledge in crypto and the technologies needed. 
Chelsea Pan - Project manager, leading backend development (AWS, writing MySQL queries)
Rayyan Shaik - frontend?
Marc Vaz - work across stack (backend and frontend)

We will collaborate using notion/google docs to document and write out our pipeline. We will use github to share and produce code

### Risks and Mitigation
Currently, our biggest risk is using WalletConnect API to have the user login. We’re not exactly sure how we can track which user is logged in to then track their data. If we can’t figure this out before the due date, we may have the user find their own user id and just input it into the extension. 

---

## Milestones and Timeline
- **Week 1:** Determine tech stack, all technologies needed (APIs), workflow. Develop barebones MVP. No Backend, no Database. Model with users manually inputting their address and their api key. Write API calls and embed them into backend.js
- **Week 2:** Begin building the backend. Write out all necessary queries and read all documentation for the APIs needed.Set up AWS RDS and learn how to set up a chrome extension. Determine table schemas, how many tables needed, what info needs to be stored. 
- **Week 3:** Continue backend development. Begin building the frontend, looking into any UI libraries needed to display tables and graphs for the extension. 
- **Week 4:**  Connect backend to the frontend. Determine logic like what happens when you click on something, what happens in the backend?
