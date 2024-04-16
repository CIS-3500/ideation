# Chrome Extension Idea: TypeMaster (tentative)

## Authors

Tiffany Lian, Alexander Dempsey, James Huang, Sanya Shetty

## Problem Statement

Many application portals require users to meet word count limits which can be both challenging and demotivating. Without any built-in word count features on the portal users would have to resort to external tools like pasting into Google Docs which is inefficient. Moreover, integrating AI-powered semantic analysis and real-time analytics into the user interface could streamline the process, providing insightful feedback and enhancing productivity and user experience.

## Target Audience

- The target audience for WordCounter includes:

- Students working on assignments with word requirements set by their instructors.

- Editors and Proofreaders who want to estimate the time required for a task.

- Applicants applying to jobs, clubs, or colleges who have prompts with word requirements.


## Description

TypeMaster is a portable writing assistant that provides word counter, writing analytics, and helps users visualize their writing goals on any website, 

## Selling Points

1. Allows uninterrupted workflow, accessible from within the tab.
2. Achieve writing milestones effortlessly by setting customizable word count goals and receiving visual prompts as you progress.
3. Persistent settings across browsing sessions and websites
4. Maximize productivity with quick and easy access.
5. Accurate word counts and analytics displayed in a compact, unobtrusive manner.
6. OpenAI API integration which provides you feedback on your professional applications.

## User Stories

1. As a job or college applicant, I want to accurately measure the word count of my responses to application prompts using a Chrome extension, so I can ensure my answers meet the specified word limits and effectively communicate my qualifications and ideas to potential employers or admissions committees.
2. As a researcher, I want to keep track of the word count of my manuscripts and academic papers stored in online repositories like Google Scholar, so I can ensure they meet the word limits for journal submissions and conference presentations.
3. As an editor, I want to assess the length of client submissions in various formats (such as PDFs or webpages) using a Chrome extension, so I can accurately estimate the time and effort needed for editing and proofreading.
4. As a blogger, I want to monitor the word count of my blog posts in WordPress, so I can maintain consistency in post length and optimize my content for search engines.
5. As a journalist, I want to track the word count of my news articles in online publishing platforms, so I can ensure they fit within the allotted space and meet editorial guidelines.
6. As a translator, I want to use the Chrome extension to count the words in a passage of text that I am translating, allowing me to estimate the time and effort required for the translation process.
7. As a creative writer, I want to meet daily word count goals and track my progress through the WordCounter Chrome Extension, leveraging its AI-powered semantic analysis to receive insightful feedback. This will help me maintain discipline, refine my writing skills, and consistently achieve my writing targets.
8. As a language learner, I want to utilize the Chrome extension to count the words in texts or articles in my target language, helping me track my vocabulary acquisition progress and understand the complexity of different texts.
9. As a teacher, I want my students to use the Chrome extension to count the words in their written assignments, enabling them to practice writing within specified word limits and improve their writing skills.
10. As a social media manager, I want to use the Chrome extension to count the words in my social media posts or captions, ensuring that my messages are clear and concise within the character limits of each platform.
11. As a job applicant crafting my cover letter on an online application form, I want to receive instant feedback on the tone and clarity of my writing so that I can improve its impact and increase my chances of getting hired.
12. As an academic researcher drafting abstracts for my papers, I want to ensure my writing is concise and clear, leveraging AI feedback to refine my abstracts before submission.
13. As an editor proofreading submissions, I want to quickly estimate the length of texts I'm working on so that I can better manage my workload and deadlines.
14. As a grant writer, I want to refine my grant applications with AI-powered insights to increase the likelihood of receiving funding for my organization.
15. As a college applicant, I want a personal assistant to provide immediate feedback on the strength of my writing, and provide me feedback on how I can make my writing more effective.

## Notes

## References & Inspiration

Grammarly

## Technical Details

### User Interface

Main interface components would include:
- Popup Window: After clicking the TypeMaster icon in the Chrome toolbar, users will see a compact, visually appealing popup window. This window displays the current word count of the highlighted text or the entire text field in focus. It will also include tabs for settings, writing goals, and feedback.

- Context Menu Integration: After right-clicking on any selected text within Chrome, users can access TypeMaster's features directly from the context menu. Options like "Analyze Word Count," "Set Goal," and "Get Writing Feedback'' will be accessible.

- Goal Tracking Visualization: Users can set word count goals for their projects. A progress bar in the popup window will visually show how close they are to reaching these goals, changing color from red to green as they progress.

- Real-time Feedback Alerts: As users type, small, notifications or visual cues can appear on the edge of the browser window, providing instant feedback or encouragement when they reach certain milestones or if the AI detects areas for improvement in clarity or tone.

- Settings and Customization Panel: Within the popup, a settings tab allows users to customize their TypeMaster experience, adjusting preferences for notifications, feedback sensitivity, and which types of analytics they find most useful.



### API, Libraries, and Frameworks

_[- List any APIs, libraries, or frameworks that you plan to use in your Chrome Extension.]_
OpenAI API
_[- Include links to the documentation or other relevant resources.]_
the Snippet Collector: https://github.com/jlumbroso/chrome-extension-text-collector 
the QuicklyGPT extension: https://github.com/zealotjin/quicklygpt-extension/ 
_[- Explain very briefly how you will use these tools in your project, one sentence per item.]_
OpenAI API will be used for semantic analysis and feedback for user highlighted text.
Snippet Collector provides an example of a built Chrome Extension as well as highlight detection and making extension available in context menu.
QuicklyGPT provides example of extension working with ChatGPT.

### Data Storage

Data to be stored
 All data should be stored locally - we don’t want to hold any API keys, key-logs, et.

## Project Management

### Collaboration and Task Allocation

_[Select a Leader, who will make final decisions on the vision of the project; and a Manager, who will oversee the project management and ensure all team members have everything they need to contribute effectively. List the remaining team members and their roles.]_

- **Leader:** James Huang
- **Manager:** Tiffany Lian
- **Remaining Team Members:** [Alexander Dempsey, Sanya Shetty]

_[Provide a brief overview of what each team member will work on. How will you collaborate on this project? Will you use to communicate and share code?]

Responsibilities:
James Huang
OpenAI API Integration
Frontend, UI/UX Figma 
Tiffany Lian
Highlighting Mechanics
QA: Testing/Debugging
Sanya Shetty
React
Graphic Design 
Alexander Dempsey
QA: Testing/Debugging
Deployment and Packaging

Tools and Platforms
	Github
	Figma
	OpenAI/HuggingFace

### Risks and Mitigation

_[Identify potential risks that could affect the development of your Chrome Extension. How will you mitigate these risks? What is your contingency plan if things don't go as expected?]_

Time
Alex is in PER and James is in Penn Boxing Fight Night + has Spring Fling & other commitments to perform for his band – Get things done on TIME!
Solution: reduce scope where needed
Start simple → complex 
Security 
User trust in giving us their key data and OpenAI keys
 Debugging 
Less experience overall in Git and Google Chrome Extension frameworks, might need more time and help debugging 
Solution: Ask TAs! Who wants to spend 17 hours on StackExchange…
Solution: Steal word highlighter from plugin demonstrated in class
Devil in the details
How to take care of trivial words we don’t want to count (space bars, ?/./punctuation in general, do we want different modes of counting)
Solution: testing and brainstorming! 
Bonus Solution: Make it cute for E.C.

### Milestones and Timeline

_[- Week 1: Figma mockup, Take apart a chrome extension (to be able to build one), Assign Roles, research libraries to make chrome extension aesthetic]
- Week 2: First Interactive Prototype, Reconvene on Features, Testing
- Week 3: Second Interactive Prototype, First finalized draft, Testing
- Week 4: Working on pull requests/comments, Packaging, Fixing up UI/UX, Medium post]_
