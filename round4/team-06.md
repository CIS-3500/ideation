# Chrome Extension Idea: LazyReader

## Authors

Rohan Kamat, Emma Lee, Kevin Lee, Annie Wang

## Problem Statement

The LazyReader Chrome extension aims to streamline information gathering and comprehension for students, researchers, and individuals by integrating ChatGPT's capabilities directly into the browser. Sometimes articles or text give an unnecessary amount of detail, which can cost readers a lot of time and effort. The LazyReader Chrome extension addresses the challenge of information overload and the high time cost associated with digesting lengthy online articles, papers, or reports. LazyReader incorporates features such as text summarization, analysis, and question generation so users can efficiently extract key insights from web pages without the need to navigate away.

## Target Audience

Lazy Reader mainly targets students and general internet users who regularly encounter lengthy textual content while browsing the web. These individuals seek to gain a base-level understanding of information with minimal effort. They value their time and seek efficient ways to absorb information. 

## Description

LazyReader provides users with a seamless solution for digesting textual content on web pages. It is a Chrome extension designed to empower users to instantly summarize the content of any webpage with a simple click. By leveraging ChatGPT's advanced language processing capabilities, users can effortlessly request summaries, key terms, and/or reflection questions based on the text present on any webpage they visit. This extension aims to help users understand the gist of various topics and enhance their browsing efficiency.

## Selling Points

1. Time Efficiency: Dramatically reduces the time required to understand and digest extensive online articles, papers, and reports.
2. Assisted Comprehension: Highlight key points and themes, giving users supplemental tools when trying to understand complex subjects.
3. Customizable Summaries: Offers adjustable summary lengths and tone, allowing users to choose the depth of detail they want.
4. Engagement and Interaction: Generates summaries and questions based on the text to encourage deeper thinking and engagement with the content if the user desires.
5. Ease of Use: Integrates seamlessly into the browser experience, enabling users to access its features on any webpage with minimal disruption.

## User Stories

1. As a student preparing for exams, I want to summarize lengthy articles I find online so that I can review key concepts more efficiently.
2. As a busy individual, I want to generate questions from articles I read online so that I can better reflect on my understanding of the content.
3. As a casual reader, I want to quickly summarize news articles I come across so that I can stay updated on current events without spending too much time.
4. As a language learner, I want to analyze and generate questions from online articles in my target language so that I can improve my comprehension skills.
5. As an educator, I want to generate questions from educational material so that I can create quizzes and tests more efficiently.
6. As a marketer, I want to analyze consumer feedback and reviews so that I can understand customer sentiment without reading every comment.
7. As a project manager, I want to condense project documentation so that my team can grasp essential details without reading every page.
8. As an investor, I want to summarize financial reports so that I can quickly assess investment opportunities.
9. As an academic, I want to generate questions about the articles I read so that I can prepare for discussions and presentations.
10. As a book club organizer, I want to summarize book reviews and author interviews from various websites, so that I can provide general information to quickly debrief club members.
11. As a social media manager, I want to consolidate user comments and feedback on social media posts, so that I can identify popular topics and trends to inform my content strategy.
12. As a student conducting research, I want to extract key terms and their definitions from academic articles and textbooks, so that I can generate a simple review list to remind me of what topics I’ve looked at.
13. As a researcher conducting literature reviews, I want to understand the main ideas and concepts of the papers I’m reviewing fast, so that I can more productively select the most relevant papers.
14. As a student preparing for standardized tests, I want to learn important vocabulary words and their definitions from reading passages and study materials, so that I can improve my performance on vocabulary-based questions.
15. As a professional attending industry conferences and seminars, I want to quickly grasp the meaning of specialized terms and acronyms used in presentations and discussions, so that I can actively participate in conversations and networking opportunities.
16. As a journalist covering diverse topics, I want to quickly understand the meaning of technical terms and specialized terminology used in interviews and press releases, so that I can accurately report on complex issues and communicate effectively with my audience.

## Notes

There is a lot of functionality that could be added on to this extension, depending on if we want to make a product that is extremely good at one thing, or a product that has many features all related to summarization and generative AI analysis of webpage content. 
We plan to use OpenAI’s API for summarization, given it’s reliability and extremely strong developer support.

## References & Inspiration

OpenAI’s ChatGPT

## Technical Details

### User Interface

Chrome Elements:
- Action Button
  - User clicks the extension action button to open the sidebar
- Sidebar
  - User uses the extension by interacting with UI components within the sidebar including:
  - Scrollable text boxes
  - Dropdown menus
  - Hoverable buttons
- [Potential Expansion] Separate webpage
  - User can choose to open the sidebar in its own webpage (full tab)

[Figma file](https://www.figma.com/file/ZP70Xo4z1mLCbY2uHYD8fi/LazyReader?type=design&node-id=1%3A2&mode=design&t=uT3QaqEEoUQaPr83-1
)

<i>(Quick overview screenshots attached)</i>

### API, Libraries, and Frameworks

- [OpenAI] (https://platform.openai.com/docs) : We will use the OpenAI API to query the content we want to summarize.
- [ReactJS] (https://react.dev) : Utilize ReactJS for the frontend to create components.
- [Some JS library for web scraping] (TBD): We plan to either find a JS library to help us with web scraping or simply draw from targeted DOM elements. 

### Data Storage

- Utilize local storage to store the user’s API Key and the previous summary/keywords/questions.

## Project Management

### Collaboration and Task Allocation

Leader: Emma Lee
Manager: Rohan Kamat
Remaining Team Members: Annie Wang, Kevin Lee

- [Kevin] Repository Setup and establishing Chrome extension foundation
  - Kevin will spearhead the initial setup of our project repository, which includes configuring the foundation, setting up the basic structure and backbone. 
- [Emma] User Interface Design
  - Emma will take charge of designing the user interface, starting with creating the Figma mocks for our extension. Then, she will develop the sidebar features, UI components for the user interface. 
- [Annie] Web Page Text Extraction 
  - Annie will be responsible for researching and implementing ways to extract text from webpages. This includes researching the appropriate JavaScript libraries for text extraction, manipulation DOM to access specific text elements, and ultimately implementing text extraction. 
- [Rohan] OpenAI API Integration and Prompt Engineering 
  - Rohan will be responsible to initiate the integration with OpenAI API and craft the prompts that will work the best for generating summaries. This includes setting up the API calls within our extension, experimenting with different prompt structures to achieve the best summaries, and ensuring our extension interacts efficiently with the API. 

To ensure effective collaboration and communication throughout the project, we plan on using the following platforms: 

- Github: We will use it for code sharing and allowing everyone to collaborate effectively. 
- Slack: We will utilize Slack for meeting coordinations, general communications, check-ins, updates, and team discussions. 
- Google Meets: In addition to in-person meetings, we will be utilizing Google Meets to meet virtually as needed throughout the course of the project. 

### Risks and Mitigation

- Limited time to meet which may cause duplication of work. To prevent this, we will try to meet up during class time to ensure that communication is swift.
- Having issues with setting up the environment. Because everyone is new with the development of Chrome extensions, there may be some technical issues trying to use ReactJS to create extensions. If there are issues, we can ask the TAs or browse the internet to find solutions or tutorials to set up the environment.

### Milestones and Timeline

<b>Week 1:</b>
- [Kevin] Task 1: Set up repo & Configure chrome extension foundation (ex: manifest file)
- [Annie] Task 2: Investigate how to approach grabbing webpage text
  1. JS library
  2. Manipulate DOM elements
  - Decide what specific elements we want to target
- [Emma] Task 3: Finish Figma mocks & Build sidebar base UI component
- [Rohan] Task 4: Initiate OpenAI API usage & Start prompt engineering

<b>Week 2:</b>
- [Kevin, Emma] Task 5: Build additional UI components (buttons, dropdowns, etc.)
  - [Kevin] Task 5.1: Build default UI (text-based, more accessible, simpler look)
  - [Emma] Task 5.2: Build display UI (icon-based, less accessible, gimmicky) 
- [Annie] Task 6: Write code to grab webpage text
- [Rohan] Task 7: Finalize prompts & Start writing logic to make OpenAI requests
  - Can make requests on “dummy” text since webpage text will not be ready

<b>Week 3:</b>
- [Kevin, Emma] Task 8: Combine UI elements to support full functionality
- [Annie, Rohan] Task 9: Combine webpage scraping + OpenAI request logic
- [Kevin] Task 10: Draw from local storage to keep API key & previously generated summaries
- [Everyone] Task 11: Test

<b>Week 4:</b>
- [Everyone] Task 12: Confirm working functionality & polish
- [Everyone] Task 13: Get ready for publishing & Ensure documentation is up to date
