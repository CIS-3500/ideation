# Chrome Extension Idea: exTimesion

## Authors

Duriya Rehan
Max Mercado
Andrew Zhen
Rayan Yu

## Problem Statement

Many individuals struggle with time management and productivity due to unintentional, excessive time spent on various websites. There is a need for an intuitive tool to help users analyze their browsing habits and increase the barrier to get distracted.

## Target Audience

- Students who need to manage their study time effectively.
- Professionals who want to minimize time-wasting websites during work hours.
- Anyone looking to improve their digital habits and productivity.

## Description

exTimesion is a Chrome extension that helps users track and analyze the time they spend on different websites. It provides detailed analytics on daily, weekly, and monthly browsing habits, identifying the most used websites, trends in usage, new and abandoned sites, and more. This information helps users understand their digital behavior and make informed decisions to improve their time management and productivity.

The extension further allows users to block websites that may be a detriment to browsing habits during work hours. 

## Selling Points

1. Easy time tracking: automated time logs for user activity. All operations run in the background with no disturbance or needed input from a user.
2. Detailed analytics: users can receive comprehensive reports on website usage across days, weeks, months, and years. Rigorous splits on usage cycles, common patterns, and various time-wasters enable easy understanding of trends and personal activity.
3. Customizable Alerts: Users can set time limits for specific websites and receive alerts when they exceed these limits.

## User Stories

<!-- 1. As a person who works from home, I want to decrease the ease with which I can visit distracting sites to make myself more accountable -->
1. As a chronic doom-scroller, I would like auto-interrupt ads on a semi-random timer to break me out of habitual social media use
<!-- 3. As a knowledge-worker, I would like time-tracking for sites that I have as my active tab so that I can more effectively assess how I am spending my time online -->
2. As a habitual online shopper, I would like the option to have an ad-free timer so that I do not view ads that might distract me even further
3. As a casual browser, I would like functionality to block only certain pages on sites so that I can still use productive parts of a site and avoid distracting parts
4. As a user, I would like an easy-to-use block-list so that I can easily add distracting sites when I find them
<!-- 7. As a student, I want a "crunch mode" that increases ad duration so there is an increased incentive to avoid distracting sites -->
5. As a user prone to mindless browsing, I want an option to include constructive activities for a break instead of ads to avoid introducting more advertising into my life
6. As a parent, I want to restrict which ads are shown to avoid inappropriate content for my child
7. As a freelancer, I want to schedule working and not working hours to automatically restrict my browsing during work hours
8. As a student, I want to see how much time I'm spending on educational vs. entertainment sites so that I can adjust my study habits for better academic performance.
9. As a freelancer, I want to monitor the time spent on different project-related websites so that I can bill my clients accurately.
10. As a parent, I want to track the time my child spends on various websites so that I can ensure they are using the internet safely and productively.
11. As an individual looking to reduce procrastination, I want to set time limits for certain websites and receive notifications when I exceed them so that I can manage my time better.
12. As a user concerned about privacy, I want to ensure my data is stored locally and not shared with third parties so that I can maintain control over my personal information.
13. **As a project manager**, I want to track the amount of time my team spends on research and collaboration websites so that I can improve our project timelines and efficiency.
<!-- 17. **As a habitual online shopper**, I want to monitor the time I spend on shopping sites each week so that I can limit my impulse buying and focus more on saving money. -->
<!-- 18. **As a content creator**, I want to understand how much time I spend on social media platforms versus content creation tools so that I can better allocate my time to productive work. -->
14. **As a digital marketer**, I want to analyze the time spent on different advertising platforms and competitor websites so that I can optimize our marketing strategies and competitive analysis.
15. **As someone trying to improve sleep habits**, I want to track the time I spend on electronics before bedtime so that I can reduce my screen time and improve my sleep quality.

## Notes

 - Consider implementing a feature for shared devices where each user can have their own profile.
 - Explore the possibility of integrating with other productivity tools or platforms for a more holistic view of the user's time management.
 - Regular updates and improvements based on user feedback can help the extension stay relevant and useful.

 This strategy may be very easy to circumvent if the block-list is easily modifiable. There may need to be protections against editing which sites are blocked.

## References & Inspiration

https://zapier.com/blog/productivity-extensions-for-chrome/
https://old.reddit.com/r/chrome/comments/18vzy7g/what_are_your_favorite_productivity_extensions/
https://old.reddit.com/r/chrome_extensions/comments/15xg1vv/extensions_for_productivity/
[Tab for a cause](https://tab.gladly.io/)
[Freedom](https://addons.mozilla.org/en-US/firefox/addon/freedom-website-blocker/)

## Technical Details

### User Interface

_[Describe the user interface of your Chrome Extension: What will users see when they interact with your extension? How will they interact with the extension? You can include rough sketches or wireframes to illustrate your design, but name your files `<project id>-ui-1.png`, `<project id>-ui-2.png`, etc.]_

[View POC](https://github.com/rayan-yu/exTimesion/blob/main/IMG_D4ECF3952792-1.jpeg)

_[Describe which Chrome UI/UX elements you will use in your extension, such as pop-ups, context menus, browser actions, omnibox, sidebar, etc.]_

We would use pop-ups to show specific page statistics/breakdown, and we would allow the user to open up a larger sidebar to show the entire dashboard of statistics, if they'd like to see a more detailed breakdown.

### API, Libraries, and Frameworks

Tabs API (chrome.tabs): This is crucial for managing tabs within Chrome. We plan on using it to listen for tab activation, creation, update, and removal events. This way, we can start or stop the timer based on the user's activity in each tab.

Windows API (chrome.windows): Similar to the Tabs API, but for managing browser windows. It's important for understanding when a user switches windows, which can affect how we track time spent in tabs.

Storage API (chrome.storage): This API is essential for saving data locally on the user's machine for persistent storage. We would probably use this to store the amount of time spent on each tab, allowing the extension to maintain records between browsing sessions.

chrome.idle: Detects when the user is idle, which can help in pausing time tracking when the user is not actively browsing.
Content Scripts (chrome.contentScripts): While not directly involved in time tracking, content scripts can be used to interact with the content of a web page. For example, we’re interested in showing an overlay on the tab that's currently being timed or inject specific elements to provide feedback to the user.

Chart.js: simple yet flexible JavaScript charting library that can be used to display analytics data through line charts, bar charts, etc.

D3.js: more complex and powerful library for data visualization that allows for highly customizable graphics. It's useful if you need more advanced visualizations.

Moment.js: now considered a legacy project in maintenance mode, it's still widely used for parsing, validating, manipulating, and displaying dates and times in JavaScript.

Node.js: running JavaScript code outside of a browser.

Npm: managing the project's dependencies.

Date-fns: modern alternative to Moment.js that offers a comprehensive, yet simple and consistent toolset for manipulating JavaScript dates in a browser & Node.js, to help in dealing with dates and times for analytics purposes.

Jest: Javascript unit testing.

Permissions: In the extension's manifest file, you'll need to declare permissions to use these APIs, including "tabs", "storage", "windows", and any other permissions necessary for your specific functionality.

Page Action / Browser Action: These APIs allow the extension to have an icon in the Chrome toolbar or next to the address bar, which users can interact with to view stats or change settings.


### Data Storage

Data to Store
Tab Information: This includes the tab ID, window ID (since a user can have multiple windows), and the URL of the tab. The URL helps identify the website, but for privacy and simplicity, you might choose to store only the domain name.

Time Spent: The amount of time spent on each tab. This could be in the form of a timestamp for when the tab became active and when it was closed or switched. Calculating the difference between these timestamps can give you the total active time spent on the tab.

Sessions: If you want to track browsing sessions, you might also store session identifiers along with start and end times for each browsing session.

Data Models
Tab Model
Tab ID: Unique identifier for each tab. (Primary Key)
Window ID: Identifier of the window the tab belongs to.
URL/Domain: The domain name of the website open in the tab.
Active Time: The total active time spent on the tab. This could be an accumulation of all active periods within a session.

Session Model
Session ID: Unique identifier for each browsing session. (Primary Key)
Start Time: Timestamp when the session started.
End Time: Timestamp when the session ended.
Tabs: A list or array of Tab IDs active in the session.

Time Entry Model
Entry ID: Unique identifier for each time entry. (Primary Key)
Tab ID: Linked to the Tab Model.
Start Time: Timestamp when the tab became active.
End Time: Timestamp when the tab was closed or switched.
Duration: Calculated duration based on Start Time and End Time.


## Project Management

### Collaboration and Task Allocation

- **Leader:** Rayan Yu
- **Manager:** Max Mercado
- **Remaining Team Members:** Duriya Rehan, Andrew Zhen


_[Provide a brief overview of what each team member will work on. How will you collaborate on this project? What tools or platforms will you use to communicate and share code?]_

Chrome extension backend: Figure out Tab/Window tracking logic, pick/learn APIs to use to track time spent on window and tabs open

Rayan + Andrew

Chrome extension backend: Database schema creation, add/remove/access calls, how to structure js routes from front-end

Max

Chrome extension frontend: popups for specific website details, sidebar for more comprehensive data. Basically learn JS/CSS/React for how to format a pop-up chrome extension and how it looks

Duriya + Max



### Risks and Mitigation

#### 1. Privacy Concerns
Risk: Users may be concerned about the tracking of their internet usage, leading to privacy issues and potential backlash.
Mitigation: Clearly communicate the data collection process, ensuring transparency. Implement strict privacy controls, such as anonymizing data and not storing sensitive information. Offer users control over their data, including options to delete it.
Contingency Plan: If privacy concerns still arise, be ready to adjust data collection practices based on user feedback and possibly consult with privacy experts to improve privacy measures.

#### 2. Performance Impact
Risk: The extension could slow down the user’s browser by using too many resources, leading to a poor user experience.
Mitigation: Optimize code for efficiency, ensuring minimal impact on browser performance. Regularly test the extension’s performance across different devices and browser versions.
Contingency Plan: If users report performance issues, prioritize updates that optimize resource usage, even if it means rolling back some features temporarily to maintain a good user experience.

#### 3. Data Security
Risk: Collected data might be vulnerable to breaches or unauthorized access.
Mitigation: Implement robust security measures, including encryption for stored data and secure communication channels for data transmission. Regularly update security protocols in response to new vulnerabilities.
Contingency Plan: Develop a response plan for potential data breaches, including immediate security audits, notifying affected users, and working with cybersecurity experts to prevent future incidents.

#### 4. Browser API Changes
Risk: Updates to Chrome’s APIs or policies could break the extension’s functionality or make it non-compliant.
Mitigation: Stay informed about upcoming changes to Chrome’s extension development guidelines and APIs. Maintain a modular architecture so you can quickly adapt to API changes without a complete overhaul.
Contingency Plan: If an API update significantly impacts the extension, communicate transparently with users about potential delays in functionality updates and work diligently to adapt the extension to new requirements.


### Milestones and Timeline

#### Week 1: Initial Setup and Planning
Task 1: Project Setup - Establish the project structure, set up a version control system (e.g., Git), and prepare the development environment.
Task 2: Requirements Gathering - Finalize the feature list, user stories, and acceptance criteria for the extension. This includes defining privacy measures, data storage needs, and the initial design for the user interface.
Task 3: Design Mockups and Architecture - Create initial design mockups for the user interface and outline the extension's architecture, focusing on how components interact, data flow, and storage.

#### Week 2: Core Development Begins
Task 4: Implement Tracking Logic - Develop the core functionality to track time spent on tabs, including activating and deactivating timers based on tab focus.
Task 5: Data Storage Implementation - Set up the local storage schema for storing tab time data securely and efficiently.
Task 6: Basic UI Implementation - Start building the user interface based on the design mockups, focusing on a minimal viable product that displays time spent on websites.

#### Week 3: Feature Completion and Initial Testing
Task 7: Complete UI Development - Finish all user interface components, including options pages, popups, and notifications.
Task 8: Integration and Functional Testing - Integrate different parts of the extension and conduct thorough functional testing to ensure reliability and performance.
Task 9: Privacy and Security Measures - Implement and test privacy controls and security measures, ensuring data is handled responsibly.

#### Week 4: Refinement and Deployment
Task 10: User Feedback Loop - Release a beta version to a small group of users or stakeholders, gather feedback, and make necessary adjustments.
Task 11: Final Testing and Bug Fixing - Address any issues identified during the beta phase, perform final testing including performance, security, and usability tests.
Task 12: Launch Preparation and Documentation - Finalize all documentation, prepare launch materials, and submit the extension to the Chrome Web Store.

### Minimum Viable Product (MVP)
Collect "all-time" tab usage statistics: (1) how long a tab was "open" (in the foreground or background) and (2) how long a tab was "active" in the foreground. 

In the pop-up view of the extension, display these statistics for the currently open tabs in the window. The pop-up should be a list of tabs open, with each tab accompanied by two basic statistics: (1) time this tab was spent "opened" and (2) time this tab was spent "active" in the foreground. Each tab will also be accompanied by a bargraph, where the x axis spans the time the tab was open and peaks in the chart represent times the tab was in the foreground. 

The extension can be expanded into a dedicated page that shows the entire dashboard. The dashboard extends the functionality displayed in the popup by allowing the user to also filter by time ranges. This is done in the backend by simply filtering on the database by timestamp. 

### Stretch Goals
- Allow the user to close tabs in the pop-up window and dashboard
- Bucketing tabs by category
 
