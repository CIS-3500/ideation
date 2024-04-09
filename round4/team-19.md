# Chrome Extension Idea: Currency Converter

## Authors

Rachel Nguyen, Peter Proenca, Hassan Rizwan, Grant Wells


## Problem Statement

Travelers, online shoppers, and professionals working across countries often face the challenge of dealing with multiple currencies. Calculating exchange rates can be tedious, error-prone, and time-consuming, especially when dealing with less familiar currencies. Our Chrome Extension simplifies this process by providing instant, accurate, and easy-to-access currency conversion directly in the browser. It eliminates the need to navigate away from the current webpage or use separate apps/tools, streamlining the user's workflow and enhancing their online experience.

## Target Audience

The target audience for our Chrome Extension includes frequent travelers, expatriates, international students, online shoppers buying from foreign websites, and professionals dealing with cross-border transactions. This audience primarily consists of individuals who regularly require quick and reliable currency conversion to budget, plan, and make informed decisions related to their international activities.

## Description

Our Chrome Extension offers a quick and easy way to convert currencies right from the browser toolbar. Users can select their base and target currencies, input the amount they wish to convert, and receive real-time conversion rates. The extension also features a customizable watchlist for monitoring favorite currencies and historical rate charts for making informed decisions.

## Selling Points

1. Real-time currency conversion for over 15 currencies, ensuring users have access to the most current rates.
2. A customizable watchlist that allows users to keep track of and quickly access their most-used currencies.
3. Historical data charts for each currency pair, helping users analyze trends and make more informed decisions.
4. A simple, user-friendly interface that enables quick conversions without navigating away from the current page.
5. Automatic detection of currencies on web pages and the option to convert displayed prices with a single click.

## User Stories


1. As a traveler preparing for a trip to Europe, I want to quickly convert the prices of hotel bookings and attractions from my local currency to euros using the currency converter extension, ensuring I stay within my budget.
2. As an online seller, I frequently deal with international customers and need to convert product prices into various currencies. With the currency converter extension, I can easily determine the converted prices to provide accurate quotes to customers.
3. As a student studying abroad, I often need to convert living expenses from my home currency to the local currency. The currency converter extension allows me to do this efficiently while managing my budget effectively.
4. As a stock trader, I need to monitor the impact of currency fluctuations on the value of my international investments. The extension provides real-time currency conversion, helping me make informed decisions about buying and selling stocks.
5. As a freelancer working with clients from different countries, I rely on the currency converter extension to accurately invoice clients in their preferred currency, simplifying the billing process and avoiding confusion.
6. As an expatriate living in a foreign country, I use the currency converter extension to convert my salary from the local currency to my home currency, ensuring I have a clear understanding of my financial situation.
7. As an e-commerce shopper, I frequently purchase products from international websites and need to know the converted prices in my local currency. The currency converter extension saves me time by automatically displaying converted prices on product pages.
8. As a cryptocurrency investor, I use the currency converter extension to quickly convert the value of different cryptocurrencies into fiat currencies, helping me track my portfolio's performance more efficiently.
9. As a small business owner with international clients, I need to convert invoices into various currencies. The currency converter extension integrates seamlessly with my invoicing software, streamlining the billing process and reducing errors.
10. As a language teacher, I use the currency converter extension to incorporate real-life examples of currency conversion into my lessons, making the learning experience more engaging and practical for my students.
11. As a remittance sender, I rely on the currency converter extension to calculate the converted amount when sending money to family members abroad, ensuring they receive the correct amount without any surprises.
12. As a frequent traveler, I want to quickly convert expenses into my home currency so that I can manage my budget more effectively.
13. As a tourist planning an itinerary, I use the currency converter extension to estimate the cost of activities and meals in different countries, allowing me to plan a budget-friendly trip without overspending.
14. As a charity organization receiving donations from around the world, we use the currency converter extension to convert donations into our local currency, enabling us to allocate funds efficiently to support our programs and initiatives.
15. As a financial advisor, I recommend the currency converter extension to my clients who travel frequently or have international investments, empowering them to make informed financial decisions and maximize their wealth management strategies.
## Notes


## References & Inspiration

https://currencylayer.com for our API of currency. 

## Technical Details

### User Interface
dropdown to input the wanting currency.
Button to convert the currency.
Popup menu for the above.
Initially, the currency values will be converted within the popup, but we hope to be able to overwrite the number and show the user the values right on the screen. 

### API, Libraries, and Frameworks

https://currencylayer.com for our API of current currency values. 
React for UI with the user. 
React Axios for connecting UI and API. 
https://www.digitalocean.com/community/tutorials/how-to-scrape-a-website-using-node-js-and-puppeteer puppeteer for datascrapping the currency/money for JS
https://cheerio.js.org/docs/api/interfaces/CheerioAPI cheerioAPI for the currency/money datascraping for HTML. 
window.getSelection to get what the user is highlighting it and potentially concert that. 
manifest.js needed for the google chrome extensions. 


### Data Storage

We don't need any data storage since we are receiving data from the API and then calculating the conversion and displaying it. 

## Project Management

### Collaboration and Task Allocation


- **Leader:** Grant
- **Manager:** Peter
- **Remaining Team Members:** Hassan Rachel


### Risks and Mitigation

Risk: Figuring how the API works and how it will interact with the actual website. Every website has different ways of presenting the price to users, in HTML or maybe even an image. So a big risk is being able to identify the price that we need to convert. 
Gran runs out of money to pay for his API. 

### Milestones and Timeline


_[- Week 1: Task 1, Task 2, Task 3
1. How different websites represent money (symbols or words)
2. Find different representations of currency from a currency website
3. Where different websites are storing their money representations (HTML/JS/Other)
- Week 2: Task 4, Task 5, Task 6
1. Implement webscarper to find the currency
2. Implement the api to currency convert
3. Implement popup to popup. 
- Week 3: Task 7, Task 8, Task 9
1. Popup elements to have currency converter in it and currency choice
2. Connect previous week's things together
3. Research how to overwrite HTML pages
- Week 4: Task 10, Task 11, Task 12]_
1. Try to overwrite HTML pages with currency converter
2. Popup elements is cleaned up
