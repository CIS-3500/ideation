# Chrome Extension Idea: Video Insight

## Authors

John Guirguis, Jake Brooks, Aditya Maddipatla, Ashwin Balaji, & Zain Khan

## Problem Statement

Many students struggle with understanding the corpus of research we’re provided to read through due to the building nature of STEM fields. As such, it’s impossible to succeed in understanding later areas of work without first grasping prior research (often this research is the product of concepts taught in fragments throughout multiple different courses in undergrad). One of the key pain points we aim to address with this product would be the need to look into and search up terms or concepts that you encounter as you read new material if you haven’t seen it before. Another would be struggling with dense wordy explanations of ideas that could be tailored for a more visual audience. Many of our users would likely be international students with multi-lingual backgrounds, and it might help them to have concepts re-explained in a language they’re more familiar with. Finally, we would hope to address recurring or important explanations (potentially for harder or more useful concepts) with bookmark abilities 

## Target Audience 

- Students who would like further elaboration or explanation of concepts that are either new or challenging for them, and which would benefit from added context

  - Visual learners who have trouble grasping concepts and processes described in literature

  - Students who are researching new topics or entering a field they’re not familiar with

  - Students who have multi-lingual backgrounds and want to be more familiar with a text by having it explained in a different language than it’s found in

- Educators who are looking for ways to make their material more engaging or visual for students

## Description

Introducing our Chrome plugin, Video Insights! Have you ever come across a word, sentence, or paragraph while browsing the web and wished you had a quick way to dive deeper into its meaning or context? Video Insights is here to enhance your online learning and exploration experience by seamlessly integrating with YouTube to provide you with a curated list of educational videos related to the content you highlight.

With Video Insights, the process is simple yet powerful. Highlight any text on a webpage, right-click, and select the "Search Videos" option from the context menu. Our plugin instantly analyzes the selected text and uses a sophisticated sorting algorithm to search YouTube for the most relevant and informative videos available.

Whether you're researching a complex topic, studying for an exam, or simply curious about a specific concept, Video Insights delivers personalized video recommendations tailored to your interests. Say goodbye to endless manual searches and hello to a smarter, more efficient way of accessing valuable video content.

********

## Selling Points (Value-Add Prop)/Features

- **Seamless Integration:** Access **Video Insights** directly from your browser's context menu for quick and convenient searches

* **YouTube Database:** Tap into YouTube's vast library of educational content to find videos that match your highlighted text.

- **Bookmarking :** Retain a **history of your previous searches** in case you want to revisit a particular topic and have the ability to bookmark particular videos  in case you have found a particularly helpful video that you want to return to at a later time 

* **Relevance Ranking:** Our advanced sorting algorithm ensures that the most relevant and informative videos are presented first, saving you time and effort.

- **Personalized Learning:** Discover new insights, explanations, and perspectives related to the content you're exploring online, with the added benefit of filters on your search results/query to customize your learning experience.

## User Stories:

1. A college student is reading an article related to one of their courses. They use the extension and find the most relevant recommended videos which help add some additional context behind the article. 

2. A software engineer is researching documentation on a newer framework. They use the extension to find videos which discuss and provide examples of the framework in use. The seamless integration of the extension allows them to quickly move back and forth from viewing recommended videos and reading the documentation. 

3. A teacher is preparing a lesson for her students. While creating the lesson, the teacher uses the Chrome extension to add additional videos to her lesson plan, further enriching their student’s learning experience.

4. A science journalist is preparing to write a complex article. They use the extension’s bookmarking feature during research to rewatch important videos when writing the article.

5. An avid learner is reading many different articles covering many distinct topics. They use the extension and particularly the bookmarking feature to keep track of interesting videos linked with each article.

6. A student is doing research for their STEM class. They use the lookup tool to see videos explaining harder concepts in the intro of the document, so they can better understand the methods of the paper

7. A student is looking for internships and is confused about job descriptions. They use the extension to find videos related to the job descriptions to help inform themselves about the skills needed for the job and associated interviews. 

8. A handy man is looking through the repair guide for a common malfunction. With the part information and the issue from the guide, they use the extension to find videos on fixing the malfunction for the specific part

9. As an international student who has a hard time grasping primary literature in English, I would like a way to access videos in my native language that explain the aforementioned concept. 

10. As an educator who is trying to inject different perspectives into their teaching, they can use this tool to browse different videos explaining a topic and therefore different ways to relay concepts to students.

11. A book club enthusiast is researching the themes of the book after reading. They use the extension to find videos related to the important themes present in the book. They curate these videos and use them at the book club meeting to facilitate discussion. 

12. As a pop-culture enthusiast who is consuming media, I want the ability to access recent videos concerning current events so that I can be more informed about their context. 

13. A medical student is reading literature on various diseases and their treatments. They use the extension to find videos which feature expert explanations and demonstrations on how to treat the diseases.

14. A basketball player is reading the play book/ or some sort of online manual and is trying to understand the various sets. They use the extension to find examples of these sets in actual basketball games. This helps them visualize the sets/plays in action. 

15. A parent is helping their child with homework, they use a Chrome extension to identify challenging concepts in their assignments to suggest age-appropriate YouTube videos that explain these concepts in an engaging manner.

# Technical Details

## User Interface

We intend to have a pop-up that captures the highlighted text that you want to query as well as different search parameters for the query such as ranking criteria and language results. After said query request the side bar will contain two tabs, one with a list of videos returned by the API ranked by relevance to query criteria with the option to bookmark specific videos. The second tab will contain a history of previously bookmarked videos for easy access in the future. Figma version of the UI to be posted within the week. 
API, Libraries, and Frameworks
Youtube API - We will use this to search and retrieve Youtube videos based on some query parameters
React - We will use this library to build our frontend application–it will be especially useful for creating windows and sidebars. 
Chrome Storage API - Used to stored bookmarked queries and video URLs.
Data Storage
We would need to store the user, their prior queries, and the videos they bookmarked. 
We can do this with a mapping of a user (taken from chrome extension directly) to their search queries and their video urls. These will be stored in chrome.storage on the user’s browser.

## Project Management

Collaboration and Task Allocation
[Select a Leader, who will make final decisions on the vision of the project; and a Manager, who will oversee the project management and ensure all team members have everything they need to contribute effectively. List the remaining team members and their roles.]
Leader: John
Manager: Aditya
Remaining Team Members: Jake, Zain, Ashwin
[Provide a brief overview of what each team member will work on. How will you collaborate on this project? What tools or platforms will you use to communicate and share code?]

We will primarily use Slack to communicate with each other. We will use the Github repository to consolidate our code in one place.
John: Figma and helping with React 
Aditya: Chrome storage and help with React design.
Jake: React frontend design and integration of YouTube API.
Zain: Youtube API integration and developing backend
Ashwin: Implementing sidebar in React, filtering 


## Risks and Mitigation

[Identify potential risks that could affect the development of your Chrome Extension. How will you mitigate these risks? What is your contingency plan if things don't go as expected?]
API Limitations: The YouTube API has rate limits that could restrict the number of searches we can perform. We will mitigate this by caching search results and optimizing our search queries.
Data storage: We need to figure out how to store user data without a costly back-end through the chrome storage API. Furthermore, we need to ensure that we are following proper security protocols both when writing and reading data as well when using an api key to make calls.
Technical Challenges: Developing a Chrome extension with seamless integration and a smooth user experience may present technical challenges. We will conduct thorough testing and be prepared to adapt our approach as needed.


## Milestones and Timeline

Week 1: Test API calls, build Figma for UI
Week 2: Build Skeleton Code for frontend structure, implement basic (unfiltered) API calls
Skeleton code = grab highlighted words, show side panel, search bar pop-up
Basic storing of data in Chrome storage. 
Week 3: Add SideBar to Frontend and Filters in sidebar. Add user set-up
Week 4: Play Video in sidebar and filter search. Add extra filters/dynamic number of filters that user might want to query on.


