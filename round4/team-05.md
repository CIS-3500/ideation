# Chrome Extension Idea: [FlyHistory]

## Authors

Melanie Chen\
Noah Erdogan\
Jason Figueroa\
Brady Zhou

## Problem Statement

Finding flights is often very time consuming, and users often find themselves opening many different tabs. FlyHistory provides an easy way to keep track of your flight search, so that you can easily revisit what you looked for in the past.

## Target Audience

- People looking for flights

## Description

FlyHistory will save the history of flights users have looked through on google flights. From there users will have the ability to filter their flight view history based on location, price, luggage type and other flight information. They can then revisit these flights saved in their history Users will also have the ability to remove flights from their history that they are no longer interested in.

## Selling Points

1. Gives a single place to look for all your previously searched flights
2. Simple and intuitive interface for users
3. Customizable filters for each user
4. Displays results in a clean and understandable fashion


## User Stories

1. As a user, I want a way to automatically save information about flights when searching the web, so that I can easily revisit them in the future.

2. As a user, I want to be able to delete specific flights in my history, so that I can hide them or clean up my interface.

3. As a user, I want to be able to filter by price, so that I can easily find all the flights within my price range.

4. As a user, I want to store the relevant information about my flight such as price, airports, time, etc., so that I can get an overview of a flight.

5. As a user, I would like to add additional settings to avoid adding specific flights to my history, so that my history only involves what I am interested in.

6. As a frequent traveler, I want to filter my flight history by destination, so that I can quickly find past searches for trips to my favorite locations.

7. As someone with specific luggage needs, I want to filter my flight history based on luggage allowances, so that I can find the most accommodating airlines without re-entering search criteria.

8. As a traveler with flexible dates, I want the option to sort my flight history by date ranges, so that I can compare prices across different periods and find the cheapest options.

9. As a user who values efficiency, I want the ability to quickly access detailed information on any flight in my history, so that I can make informed decisions without re-searching the flight.

10. As a user who often compares flights, I want the ability to compare selected flights from my history side-by-side, so that I can easily see differences in price, timing, and other relevant details
 
11. As a user with a preference for certain seats, I want to see information on seat availability and type (window, aisle, extra legroom) for flights in my history, so I can make bookings based on my seating preferences.

12. As a user who often compares flights, I want the ability to compare selected flights from my history side-by-side, so that I can easily see differences in price, timing, and other relevant details.

13. As a luxury traveler, I want to filter my flight history to show only business or first-class options, so I can compare premium travel experiences across different airlines.

14. As a parent traveling, I want to filter and sort my flight history based on family-friendly features, such as in-flight entertainment and child meal options, so I can choose the best flights for family travel.

15. As a pet owner, I want to filter my flight history by pet-friendly flights 

## Notes

Potential challenges:
1. Detecting when to extract data
2. How will we extract the data from Google Flights.

Features to highlight:
1. Automatically store information about the flights you’re looking at
2. Customization and personalization for each user and their needs
3. Simple and intuitive UI

## References & Inspiration

Other related existing products:
1. TravelArrow - https://chromewebstore.google.com/detail/travelarrow-your-virtual/coplmfnphahpcknbchcehdikbdieognn
2. Flight Fare Compare - https://chromewebstore.google.com/detail/flight-fare-compare-googl/mmhdlhieabmpkjcffmaagonallanjiad
3. CheaperThere - https://chromewebstore.google.com/detail/cheaperthere-cheap-flight/ickdpignpmjcahkjfbmfljhiglmcmchn
4. Flight Search - https://chromewebstore.google.com/detail/flight-search/dficcobpghplfppapheaenjajahhckkj


## Technical Details

### User Interface [melanie]

We plan to have our chrome extension automatically save flight information when the user is on the google flights site. When a user wants to revisit their flight history, there will be a sidebar tab which shows all of their history as well as a filter section. Once the filters are set, the user will then see flights from their history that fall under those filters.

_[Describe which Chrome UI/UX elements you will use in your extension, such as pop-ups, context menus, browser actions, omnibox, sidebar, etc.]_

We will use sidebars.

### API, Libraries, and Frameworks

React: We will be using React to develop our frontend.
Puppeteer: This is a Node.js library for web scraping, which will be used to extract data regarding the flights (https://pptr.dev) 


### Data Storage

We will need to store the relevant information about the flights that are related to what the user is searching for. This would include price, location, URL, etc.. The data will most likely be structured in a JSON format. This will be stored in local storage.

## Project Management

### Collaboration and Task Allocation

- **Leader:** [Jason Figueroa]
- **Manager:** [Noah Erdogan]
- **Remaining Team Members:** [Brady Zhou (Frontend), Melanie Chen (Backend)]

Team Member Responsibilities:
- Jason: Frontend, documentation
- Noah: Backend, documentation
- Brady: Frontend, documentation
- Melanie: Backend, documentation

We plan on using GitHub to share code and using iMessage to communicate with each other. We plan on collaborating on the project by meeting at a regular time per week to provide updates, bring up issues, and work on the project together synchronously to remain on track. 

### Risks and Mitigation

Some potential risks that could affect the development of our extension are the following:
1. Changing website structure
Flight-searching websites frequently update their user interfaces and underlying structures, which can break the functionality of the extension. To mitigate this, we can consider implementing robust error handling and monitoring mechanisms to detect changes in website structures. We can regularly update the extension to adapt to these changes promptly and utilize techniques like automated testing and version control to ensure stability across updates.


2. User data privacy and security
Handling sensitive user data such as flight preferences and history requires robust security measures to protect against unauthorized access and data breaches. To mitigate this, we can Implement strong encryption and authentication mechanisms to secure user data both in transit and at rest.

Contingency Plan:
If things don't go as expected during development or after deployment, our team should be prepared to adapt and respond effectively. We can consider implementing a simpler idea that involves using the OpenAI API to create travel plans.

### Milestones and Timeline

Week 1:

Task 1 - Set up repo with an Extension folder and a React app folder. Extension will include content.js and manifest.json. Update React app to create sidebar with content from content.js. View the sidebar by toggling on FlyHistory within My Extensions in your chrome browser. (Noah)

Task 2 - Create UI for pop-up and sidebar when on Google Flights website

Task 3 - Set up local storage

Week 2:

Task 1 - Get started with testing the product

Task 2 -  Implement checkboxes to allow users to select flights to interest, or add flight info (source, dest, price) and URL to sidebar when the bookings page is visited for a given flight

Task 3 - Update UI of sidebar given the changes in Task 2

Week 3:

Task 1 - implement tests for the feature implemented in week 2

Task 2 -  Add a new feature to the sidebar, such as grouping by price or destination

Week 4:

Task 1 - Clean codebase

Task 2 - Debug any remaining minor issues

Task 3 - Publish extension

