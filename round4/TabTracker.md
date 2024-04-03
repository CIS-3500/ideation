# Chrome Extension Idea: [TabTracker]

## Authors

Maya Chari, Arriella Mafuta, Sid Kanderi

## Problem Statement

Many people use Chrome to accomplish a variety of tasks such as work, communications, entertainment, and social media. A major problem today is that we forget to close inactive tabs when using the Internet. Moreover, when there are several tabs open in the browser, navigating through different sites can be tedious. TabTracker allows us to closely monitor our usage of different web pages and mark out tabs for closure.

## Target Audience

Our target audience is primarily students who are juggling work for many classes at once or anyone that tends to have many tabs open on their Chrome browser. 

## Description

It would provide a list of tabs that the user has open along with a 1 sentence summary of the content on each tab. Each tab will be highlighted (green, red) to indicate if that tab is currently active or inactive. 

## Selling Points

1. Users can effortlessly manage their open tabs by quickly identifying those that have been open for an extended period, reducing cluttering of tabs.
2. Scroll feature helps users see all of the tabs they have open at once.
3. Utilizing the color-coded feature, users can readily identify the tabs which are inactive.
4. Users can easily find tabs that they are looking for by reading the 1 sentence description of each tab’s content (instead of having to “guess” based on tab header on the browser)
5. With a select button, users will have the ability to close multiple inactive tabs at the same time, without having to go through them one by one.

## User Stories

1. As a user, I want to be taken directly to my desired tab by clicking on the tab description in the popup window
2. As a researcher, I want to have a clear overview of all my open tabs and their content summaries to efficiently navigate between different research topics.
3. As a user who often multitasks, I want to easily spot tabs that have been open for a long time so that I can prioritize which tabs to focus on.
4. As a developer, I want to manage tabs related to different coding projects and documentation to enhance my productivity.
5. As a project manager, I want to easily spot and close tabs related to completed or outdated projects to declutter my browser.
6. As a user, I can easily manage my tabs to avoid having tabs of the same information.
7. As a user, I want to be able to set a timer threshold such that TabTracker will close tabs which pass this threshold.
8. As a student, I want to clearly see which of my tabs are inactive and which ones are active
9. As a student, I want to easily be able to close multiple inactive tabs at once instead of individually
10. As a user I want a scroll feature that allows me to easily see all of the tabs I have open
11. As a teacher with many papers to review online, TabTracker allows me to reduce clutter on my browser by prompting me to close those papers I’ve already graded.
12. As the CEO of Google, I am tired of Chrome not doing anything to help fix my excessive tab issue and can now have an efficient browsing experience.
13. As a parent, I can get a prompt to close all the tabs my kid has opened when he is finished using my computer to play video games.
14. As a student with many classes, I want my tabs in different browsers to show up on a holistic breakdown.
15. As a student athlete, I can more efficiently get schoolwork done by closing unnecessary outdated sports-related tabs.

## Notes

Certain potential features:
Ordering tabs by most recently used
Tab grouping with color-coded columns
Implementing a search feature

## References & Inspiration

OneTab: <https://chromewebstore.google.com/detail/onetab/chphlpgkkbolifaimnlloiipkdnihall?pli=1>

SessionBuddy -
<https://chromewebstore.google.com/detail/session-buddy/edacconmaakjimmfgnblocblbcdcpbko>

## Technical Details

### User Interface

Upon activating the extension, a side panel emerges displaying the activity and inactivity of each tab. The names and contents of each tab will be arrayed vertically and ordered by most recently used. The inactive tabs will be marked by red color-coding, whereas the active tabs will be marked by green color-coding. A prompt will also emerge to close all those highlighted red tabs, with an option to deselect some or all tabs to escape deletion. Additionally, hovering over the tabs in the sidebar will allow you to directly access any said tab through clicking on it.

TabTracker implements a sidebar to display the names and contents of various tabs open and is navigable via a scrolling feature. Each tab will take up one line (two sections: website name and one-sentence summary of page content).

### API, Libraries, and Frameworks

1. Chrome Extension API <https://developer.chrome.com/docs/extensions/reference/api> : Utilized for interacting with Chrome browser functionalities like accessing tabs.
2. Chrome Extension Documentation <https://developer.chrome.com/docs/extensions>: Provides relevant information for how to build Chrome extensions and covers basics for integration.
3. React: Create and reuse UI components to make a responsive user interface for TabTracker.
4. Axios: to make HTTP request to external APIs

### Data Storage

1. Tab ID: unique identifier for each tab
2. Page title/URL: necessary for giving content to AI API or for web-scraping
3. When the tab was first opened by the user
4. What time the user was last on that tab (for more than a certain amount of time, maybe 10 seconds)
5. Summary of the content of each tab
6. User preferences: what time they think qualifies as “inactive”

Structure of Data:
Map (with tab ID as key) or array?

Data Management:
Chrome storage API: will allow us to save user preferences (chrome storage local)

## Project Management

### Collaboration and Task Allocation

- **Leader:** [Maya Chari]
- **Manager:** [Arriella Mafuta]
- **Remaining Team Members:** [Sid Kanderi]

Each team-member will work on a big task collectively each week, with distinct roles that have yet to be determined, as we will need to figure things out and react to the product implementation as we go. We will communicate through Slack and use GitHub to share code.

### Risks and Mitigation

1. We might not be able to access the data on a webpage
2. Complexity in accessing some browser functionalities

### Milestones and Timeline

Week 1: Understand the components of a chrome extension. Get basic skeleton code (files that we need)
Week 2: Backend: using chrome extension API (and potentially openAI api or webscraping) to retrieve data that we need (refer to data section)
Week 3: Frontend: using react to display tab information on the chrome extension sidebar
Week 4: Adding additional features (active/inactive tabs, sorting, search)
