# Chrome Extension Idea: Currency Converter

## Authors

Akanksha Tripathy, Ruth Tilahun, Tianyi Wu, Yola Yan

## Problem Statement - TW

[Describe the problem that your Chrome Extension will solve. What are the pain points that users experience? How does your extension address these pain points?]

Our Chrome Extension solves the inconvenience, time-consuming nature, and accuracy concerns associated with manually converting currencies while browsing the internet. By seamlessly integrating into the browser, it provides real-time conversion rates, a user-friendly interface, and customization options for preferences. Users can now quickly and accurately convert currencies without leaving their current webpage, significantly enhancing their browsing experience.

## Target Audience - YY

[Identify the target audience for your Chrome Extension. Who will benefit from using your extension? What are the main characteristics of your target audience?]

The target audience for our Chrome Extension includes:

- Travelers: People who travel internationally for business or leisure and need to convert currencies regularly.

- Online Shoppers: Individuals who frequently shop from international websites and need to convert prices to their local currency to make informed purchasing decisions.

- Finance Professionals: Traders, investors, and financial analysts who require quick and accurate currency conversion for their work.

- People living in a country with a different currency than their home country, who need to convert currencies for daily transactions.



## Description - TW

[Provide a general description of your Chrome Extension idea in 2-3 sentences. Explain the main purpose and functionality of the extension.]

Our Chrome Extension is a convenient currency converter that seamlessly integrates into your browsing experience. With real-time conversion rates and a user-friendly interface, it allows users to quickly and accurately convert currencies without leaving their current webpage. Whether you're shopping online, planning a trip, or conducting business transactions, our extension streamlines the currency conversion process, enhancing your browsing experience significantly.

## Selling Points - ALL*1 each

1. Convenience. Our extension seamlessly integrates into the Chrome browser, allowing users to access the currency converter without having to navigate away from their current webpage.
2. Real-time Exchange Rates: Provide users with up-to-date exchange rates sourced from reliable data providers.
3. Record keeping: Keep track of recently used currency and previous transactions.
4. Historical Data: Let users know if exchange rate is up or down compared to historical relative rates.
5. User-Friendly Interface where our extension offers a simple and intuitive interface that allows users to input their desired currencies quickly and easily.


## User Stories - ALL * 4 each

_[List user stories that describe the main features of your Chrome Extension. Use the following template: "As a [user role], I want to [goal] so that [benefit]." Fill in the brackets with the appropriate information. Provide 15 user stories or more.]_

1. As a busy professional trader, I frequently browse international news websites to stay updated on global events. With the currency converter Chrome Extension seamlessly integrated into my browser, I can quickly convert currency values mentioned in articles without interrupting my reading flow, making it convenient to understand financial news from around the world.

2. As an avid online shopper, I often visit various e-commerce websites to browse products from international vendors. With the currency converter Extension seamlessly integrated into my browser, I can easily convert product prices to my local currency without leaving the website, saving me time and allowing for a smoother shopping experience.

3. As a student studying abroad, I regularly conduct research online for my academic projects. With the currency converter Extension integrated into my browser, I can effortlessly convert currency values mentioned in research papers and articles without navigating away from the page, facilitating my studies and helping me grasp global economic concepts more efficiently.

4. As a frequent traveler, I often plan my trips and book accommodations and activities online. With the currency converter Chrome Extension seamlessly integrated into my browser, I can convert prices displayed in foreign currencies on travel websites instantly, allowing me to budget and make informed decisions without having to switch between multiple tabs or websites.
   
5. As a government agency, I want to monitor currency fluctuations to anticipate potential economic impacts and adjust fiscal policies accordingly to maintain stability in the economy.

6. As a tax consultant, I need accurate currency conversion rates to convert income earned in foreign currencies into the local currency for tax reporting and compliance with tax regulations.

7. As a data scientist, I seek access to APIs providing real-time exchange rates to integrate currency conversion functionality into analytical tools and models for financial forecasting and risk management.

8. As a financial advisor, I require access to historical exchange rate data to analyze currency trends and provide clients with informed recommendations for currency hedging strategies and international investments.

9. As a student on a budget, I want representations of relatively cheap versus expensive currencies so that I can make responsible shopping and traveling decisions which optimize the value of my money.
    
10. As a busy individual, I want efficient conversions that happen in seconds, and allow me to switch between currencies seamlessly so that I can save time while converting currencies and don't interrupt my browsing activities.
    
11. As a responsible budgeter, I want to store my previous conversions and transactions so that I can access the previous values and currencies that I was converting between to use for my personal records later.
    
12. As a merchant of tourist products, I want to monitor changes in global currencies so that I can anticipate the willingness of different types of tourists to purchase my products.

13. As an online shopper who frequently needs to convert currencies, I want to use a currency converter in my browser that is simple and intuitive, so that I can quickly convert currencies without any confusion.

14. As a power user, I want the currency converter Chrome extension to offer customizable shortcuts or hotkeys, allowing me to perform currency conversions efficiently without relying solely on mouse clicks.

15. As a user who values aesthetics, I want the currency converter Chrome extension to have a visually appealing design with modern UI elements and smooth animations, enhancing my overall browsing experience.

16. As a user, I want the currency converter Chrome extension to offer both dark and light mode themes, allowing me to switch between them based on my preferences and reducing eye strain during late-night browsing sessions.

## Notes - AT

Since many variations of this Chrome extension already exist, it may be challenging to distinguish our product from others. Since this is a relatively simple product, I think that a potentially unique approach for us could be to make the UI especially compelling and user friendly. We are considering an option where the conversion happens automatically when one highlights a number on the webpage. An even further step would be to do an automatic conversion, the way certain translation Chrome extensions work.

## References & Inspiration - AT

We were inspired by the Currency Converter Widget Chrome extension which already exists, as a guideline of the general features which we want to include for our own Chrome extension. While we are not aiming to replicate this fully, we want to make sure we include the features that already exist in this extension and build upon them for our own project. The extension can be found here: https://chromewebstore.google.com/detail/currency-converter-widget/bnpalipgomknhgbmgelaplknnmckljaf

This extension will also be used to guide our UI improvements, since we will identify pain points in existing extensions and use them to improve our own extension. 



## Technical Details

### User Interface - RT

When users interact with the extension, they will typically see an icon in the Chrome toolbar, representing the currency converter. Upon clicking the icon, a small pop-up window will appear. This window will include:
- Input fields for the source currency amount and the selection of the source currency.
- Dropdown menus or search bars for selecting the target currency.
- Real-time conversion results displayed prominently, showing the converted amount.
- Additional settings or preferences accessible through a gear icon, allowing users to customize the extension behavior (such as language preferences, decimal precision, etc.).
- Buttons or shortcuts for quick actions, such as swapping source and target currencies, clearing input fields, accessing historical exchange rate data, and a bookmark for previous conversions saved by the user.
  
Users will interact with the extension primarily by inputting the source currency amount and selecting the source and target currencies using dropdown menus or search bars. The conversion results will be updated dynamically as users make changes, providing instant conversions. Additionally, users can customize their experience by adjusting settings or toggling between dark and light mode themes to suit their preferences.

### API, Libraries, and Frameworks - YY

_[- List any APIs, libraries, or frameworks that you plan to use in your Chrome Extension.]_
_[- Include links to the documentation or other relevant resources.]_
_[- Explain very briefly how you will use these tools in your project, one sentence per item.]_

For this Chrome Extension, we plan to use the Google Finance API to obtain currency ratios on specific dates.

Google Finance API: Documentation, Yahoo Finance API

Explanation: We will use the Google Finance or Yahoo Finance API to fetch historical currency exchange rates for the desired date, enabling users to access accurate and reliable conversion rates within the extension.

### Data Storage - AT

We may need to store the last used currencies involved in conversion for ease of the user, especially if they tend to use just a few of the currency options and do not need to scroll through the full dropdown menu. Additionally, it may be useful to store past transactions and conversions, in case a user wants to view the last value they obtained. We may be able to use a simple relational database to store this data in the backend.

## Project Management

### Collaboration and Task Allocation

_[Select a Leader, who will make final decisions on the vision of the project; and a Manager, who will oversee the project management and ensure all team members have everything they need to contribute effectively. List the remaining team members and their roles.]_

- **Leader:** Tianyi Wu
- **Manager:** Akanksha Tripathy
- **Remaining Team Members:** Yola Yan, Ruth Tilahun

_[Provide a brief overview of what each team member will work on. How will you collaborate on this project? What tools or platforms will you use to communicate and share code?]_

### Risks and Mitigation - RT

Risks:
- There may be technical challenges in implementing certain features or integrating with external APIs for currency data.
- The extension relies on third-party libraries or APIs, which could be subject to changes.

Mitigation:
- Break down complex features into smaller tasks and allocate sufficient time for troubleshooting and debugging.
- Utilize documentation and seek assistance from TAs and our instructor.
- Choose reliable and well-supported libraries or APIs with clear documentation and a history of stability.
- Have backup/ alternative libraries in place.
  
If things don't go as expected, the contingency plan may involve:
- Prioritizing the main features and functionalities to ensure that the core functionality of the extension is implemented on time.
- Considering alternative approaches or simplifications to meet the project deadline while maintaining the core value proposition of the extension.
  
### Milestones and Timeline

_[You have about four weeks to work on this project. During the project management, you will use an Agile methodology to manage your tasks. For now, provide your best estimate of the work done each week, from Week 1 to Week 4.]_

_[- Week 1: user interface design draft, research on other similar converters
- Week 2: Web scrapping for a couple of websites
- Week 3: API integration for exchange 
- Week 4: combination and testing ]_
