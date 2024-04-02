# Chrome Extension Idea: Web Styler

## Authors

Kevin Liu, Adam Gorka, Andy Li, Judah Nouriyelian

## Problem Statement

By default, in order for users to change visual elements of webpages, they must manually inspect the underlying HTML/CSS, locate the desired elements, and change their states. This process is often time-consuming, if not difficult or even impossible for inexperienced or visually impaired users. We propose this extension as a way for users to customize these elements more easily.

## Target Audience

Targeted towards visually impaired individuals, specifically for colorblind and near-blind. Our extension will adjust the style of a website so that any text is larger. In addition, any coloring/style will be adjusted so that it's more clearly visible for individuals with color blindness.

Many individuals that are color blind or visually impaired struggle with viewing web pages that are not formatted well. They would significantly benefit from a tool that enlarges text and changes colors to be color-blind friendly. 

Additionally, the extension can also be used by other people who simply want an easy way to change such features for their own personal preferences.

## Description

This extension allows users to change visual features (e.g., text size, color) on websites to suit their preferences. Giving users a way to interact with these visual elements more directly and easily, the tool can be used for a variety of purposes, from accessibility to personalization.

## Selling Points

1. Enhanced accessibility for everyone.
2. Customizable styling. Users can change the size of fonts as well as the color/filters applied.
3. Convenience. Chrome extension will be applied automatically to every webpage.
4. Compatibility. Will be compatible with any type of website.
5. Personalization. Users can create and save certain themes/styles as favorites.

## User Stories

1. As a colorblind user, I want to change the colors of various visual elements to colors that I can easily distinguish.
2. As a visually impaired user, I want to increase text size to make the text more readable.
3. As a user, I want to personalize webpages by changing colors, fonts, etc., to ones that I like.
4. As a user, I want to create certain styles that I like and save them as “favorites,” allowing me to easily apply them to other sites in the future.
5. As a user, I want to change background color to eliminate any distractions in the background.
6. As a user, I want to access some built-in themes, like dark mode and grayscale.
7. As a user, I want to use a color picker to easily choose my preferred color(s).

## Notes

[Color models in computer graphics](https://en.wikipedia.org/wiki/Comparison_of_color_models_in_computer_graphics)
* Consider using HSL or HSV to determine hue (red from yellow from blue, etc)
* See basics of color section and “determine the value ranges [of the HSV or HSB model implementation used] before attempting to interpret a value.”

Rule of thumb: Start simple and reliable. Better to have a few features that always work instead of many features that sometimes work.

Text Sizes
* In Figma presentation, TA recommends using text sizes = 18 * 1.309^k
  * where 1.309 is “half” of the golden ratio = 1.618…

## References & Inspiration

[Color blindness simulator](https://www.color-blindness.com/coblis-color-blindness-simulator/)

## Technical Details

### User Interface

The user interface of our Chrome Extension would be a browser action that opens up a sidebar (and perhaps its own page where people can change default themes, fonts, styles, and include/exclude websites from these). The sidebar should have a list of different attributes with sliders/gradients such as color, contrast, text size, theme, and toggles for things like color blindness and black and white. 

We will use a browser action that will open up a sidebar, which shows the main customization options. The extension will only use this to keep it as minimal as possible.

### API, Libraries, and Frameworks

Some libraries/resources that we plan to use include:
* [Chrome extension browser action documentation.](https://developer.chrome.com/docs/extensions/mv2/reference/browserAction) Will use this to reveal the main UI. 
* [A potential library to use for color-picking.](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/color)
* [Another potential library?](https://www.w3.org/TR/css-color-3/#hsl-color) HSL color model in CSS
* [Quick examples of potential input types](https://www.w3schools.com/html/html_form_input_types.asp)
* [Library that allows you to create responsive and element-specific CSS.](https://github.com/marcj/css-element-queries) This can be particularly useful for adjusting text sizes and layout changes based on the user's customization.
* [JavaScript framework for building UIs.](https://vuejs.org/) Useful to develop a more complex or interactive UI for extension's settings page.

### Data Storage

We will use Chrome’s local storage to store user preferences, including:
* Websites to apply styles to
* Which styles/changes to make to those websites

This can be represented as a table, where each row corresponds to a website and each column corresponds to a saved value for a property (e.g., black for background color).

We might also create a set of pre-defined themes (i.e., sets of values for different properties) and save that in another similar table. We may let the user create and add their own custom themes to this collection.

## Project Management

### Collaboration and Task Allocation

- **Leader:** Judah Nouriyelian
- **Manager:** Adam Gorka
- **Remaining Team Members:** Andy Li, Kevin Liu

Each member will work on whichever task is the most pressing - otherwise they will work on general additional features or be flexible. The most important part of the project will be setting up the basic extension and UI, which everyone will work together on. 

We will use Slack for communication, GitHub for version control and code sharing, and Zoom for team meetings. If team members are working on different features, we can also just work on separate branches to develop each feature. 

### Risks and Mitigation

Some potential risks might include becoming behind schedule or struggling to implement our features in time. Our overall plan is to start with small features that we know we can implement in time, and then build upon that. That way, we can guarantee that our extension will be useful and usable, but may not include all of the planned features. If we aren’t able to implement some of the more advanced features, then we will drop those features that we can’t implement and focus only on getting the fundamental features to work reliably.

### Milestones and Timeline

Week 1:
* Task 1: Project Initialization (create project with basic structure)
* Task 2: Basic User Interface Development  (Design and implement the basic user interface for the extension's popup or sidebar)
  * Should finish deciding on popup, sidebar, new page, etc.
* Task 3: Implement changing the color of text (First feature and also a good warmup)

Week 2:
* Task 4: Implement Text Resizing Feature (Develop the functionality to increase or decrease text size on webpages)
* Task 5: Integration of Color Picker (Incorporate a color picker tool into the extension's UI to enable users to select custom colors for text, backgrounds, and other elements)
* Task 6: User Preferences Storage (Implement functionality to save and load user preferences, such as selected color schemes and text sizes)

Week 3:
* Task 7: Develop Predefined Themes (Create and integrate predefined themes (that users can easily apply to all webpages)
* Task 8: Custom Themes Creation (Allow users to create, save, and apply their custom themes)
* Task 9: Ensure Cross-Website Compatibility (Test and adjust the extension's features to work across a wide range of websites, focusing on common issues like overridden styles and dynamic content).

Week 4:
* Task 10: Optimize Performance (optimize the extension's performance to ensure it runs smoothly, focusing on minimizing resource usage and ensuring fast execution of scripts).
* Task 11: Final Testing and Bug Fixing (Conduct thorough testing of the extension to identify and fix any bugs or issues, ensuring all features work as intended).
* Task 12: Prepare for Deployment (Finalize the extension, including refining the UI/UX, updating the documentation, and preparing the package for deployment)
