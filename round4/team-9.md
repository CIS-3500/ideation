# Chrome Extension Idea: FocusTabs

## Authors

Eshan Singhal, Anirudh Bharadwaj, Gui Feitosa, Kofi Addae-Sakyi

## Problem Statement

When you’re working online, especially when trying to multitask, it's extremely easy to get lost in a sea of 30-40 tabs that leaves you floundering. Cluttered tabs not only reduce your productivity but can also leave you more stressed and frustrated, as you struggle to keep track of everything. 

## Target Audience

Our target audience is primarily high school and college students, who often have to manage multiple assignments for various classes.

## Description

This Chrome extension will allow you to manage your Chrome tabs by grouping them according to their core purpose (studying for CS, ECON, or MATH, group projects, job hunting, and even simply leisure).

## Selling Points

1. Increase productivity by only having tabs open tailored to your specific task.  
2. Ensure that your tabs are efficiently organized so that you always know where your work for a particular assignment/activity can be found.
3. You can seamlessly navigate between different tasks without needing to close and open a ton of tabs.
4. Tab grouping suggestions allow you to further optimize your workflow.
5. Analytics on your tabs allows you to examine your overall time spent on such tasks (e.g. which tasks demand more/less of your time, when are you most/least efficient during the day, etc).

## User Stories

1. As a high school student, I want to group my Chrome tabs by assignment or class so that I can focus on one task at a time without feeling overwhelmed.
2. As a college student, I want to organize my tabs based on different research topics so that I can easily switch between projects without losing track.
3. As a multitasking user, I want to be able to collapse and expand tab groups to declutter my browser window and reduce distractions.
4. As a busy student, I want the extension to suggest tab grouping based on my browsing history and open tabs to streamline my workflow.
5. As a user with a heavy workload, I want to be able to label tab groups with custom names to keep my tasks organized and easily identifiable.
6. As a user managing multiple group projects, I want to share tab groups with my team members for collaboration and coordination.
7. As a user with limited screen space, I want the option to pin important tab groups to always keep them visible.
8. As a user transitioning between devices, I want my tab groups to sync seamlessly across different instances of Chrome for continuity in my work.
9. As a user preparing for exams, I want to create temporary tab groups for each subject to efficiently review relevant materials.
10. As a user prone to distractions, I want to set timers for tab groups to automatically close them after a specified period to stay focused.
11. As a user conducting online research, I want to save tab groups as bookmarks for future reference and quick access.
12. As a user collaborating on group projects, I want to be notified when changes are made to shared tab groups by other team members.
13. As a user managing personal and academic tasks, I want the option to color code tab groups for better visual organization.
14. As a user working on multiple assignments simultaneously, I want to be able to rearrange tab groups to prioritize tasks based on urgency.
15. As a user seeking to optimize my workflow, I want the extension to provide analytics on tab usage and time spent on different tasks.
16. As a user with a preference for minimalistic interfaces, I want the option to hide tab group labels to reduce visual clutter.
17. As a user with a tendency to forget tasks, I want to set reminders for specific tab groups to ensure I don't miss deadlines.
18. As a user currently searching for job opportunities, I want to separate my tabs on each company I am applying to, as to ensure I won't mix information about them.

## Notes

N/A

## References & Inspiration

N/A

## Technical Details

### User Interface

Users will interact with a sidebar.

### API, Libraries, and Frameworks

**Chrome Tabs API:** We plan to use this to actually interact with browser tabs, retrieving them and grouping them together.

**OpenAI API:** We plan to use this to figure out automated suggestions for groupings of tabs that users frequently visit.

**Selenium:** We plan to use this library to figure out how to scrape login data from websites and log in for the user when opening tabs for sites that necessitate logging in (ex. Canvas).

**React:** We plan to use React for the front-end visualization of our application.

**Node.js:** We plan to use Node as the backend for our application (for data processing, user authentication, and integration with other APIs).

**Google Analytics:** We plan to use Google Analytics to examine the user's time-spending information and generate insights through them.

### Data Storage

Each tab group should have its own model to store information such as:
- _Group name:_ A descriptive name for the tab group.
- _Group color:_ If color-coding is supported, store the chosen color.
- _Tabs:_ An array or list of tab objects representing the tabs contained within the group.
- _Time spent in tab group:_ For remainders, insights, etc.
- _Optional properties:_ Any additional properties related to the tab group, such as creation date, pinned status, etc.

Each tab within a tab group should be represented by a model containing details like:
- _Tab URL:_ The URL of the tab.
- _Tab title:_ The title of the webpage.

## Project Management

### Collaboration and Task Allocation

- **Leader:** Eshann (OpenAI API Integration)
- **Manager:** Gui (Tab Grouping)
- **Remaining Team Members:** Anirudh (UI/UX), Kofi (Google Analytics)

### Risks and Mitigation

**Complexity of Integration:** Integrating multiple APIs (Chrome Tabs API, OpenAI API, etc.) and frameworks (React, Node.js) may lead to technical challenges and delays.

**Mitigation Strategy:** We will try to mitigate this by breaking down our development tasks into smaller, manageable chunks, as well as conducting thorough research of each API/library before implementing anything involving it. We also plan to continually seek guidance from Professor Lumbroso and the TAs for any technical issues encountered.

**API Limitations or Changes:** The APIs used in the extension may have limitations or undergo changes that could impact functionality or compatibility.

**Mitigation Strategy:** We will do our best to Implement error handling and fallback mechanisms to handle API limitations or failures.
**Security Vulnerabilities:** Inadequate handling of user data or authentication mechanisms may expose our extension to security risks such as data breaches or unauthorized access attempts.

**Mitigation Strategy:** We will do our best to implement robust authentication and authorization mechanisms to protect user data.

### Milestones and Timeline

**Week 1 (ending 4/7):**
1. Set up project repository and initial file structure.
2. Define basic UI layout and functionality using React.
3. Research and familiarize ourselves with Chrome Tabs API and OpenAI API.
4. Begin initial implementation of Chrome Tabs API integration to retrieve and manipulate browser tabs.

**Week 2 (ending 4/14):**
1. Continue implementing Chrome Tabs API integration for tab grouping functionality.
2. Research and experiment with OpenAI API for automated tab grouping suggestions.
3. Begin designing and implementing the backend with Node.js for data processing and user authentication.

**Week 3 (ending 4/21):**
1. Complete implementation of tab grouping functionality using Chrome Tabs API.
2. Integrate OpenAI API for automated tab grouping suggestions.
3. Implement basic user authentication and data storage functionalities in the backend using Node.js.

**Week 4 (ending 4/28):**
1. Refine UI/UX design based on feedback and usability testing.
2. Implement additional features such as tab group sharing, reminders, and analytics.
3. Perform comprehensive testing and debugging to ensure the extension functions smoothly across different scenarios and environments.
4. Prepare for deployment by optimizing code, updating documentation, and finalizing project assets.
