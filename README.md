# Styling Documentation
A resource of general guidelines for organizing, creating and making styling decisions. Especially geared towards developers working on hobby or personal projects.

About
------
#### This is a work in progress.
This repo contains a set of documents to be considered as a default starting point for styling projects. Additionally, it aims to provide insight into how to plan and execute styling.  Empty sections indicate where resources are still being gathered and decisions made.
Hopefully this planning allows for greater ease when returning to projects after some time away from them. It also aims to aid in planning collaborative efforts.



### Reset
The reset.css sheet is the work of Eric Meyer. Credit is given at the beginning of the sheet. You can read what Meyer has to say about it [here.](https://meyerweb.com/eric/tools/css/reset/ "CSS Tools: Reset CSS")
This stylesheet removes all default browser styling and does not replace it. As such, it can be modified to provide base styles per project. This might include things such as background color and font-size.
At the beginning of the stylesheet it is noted (as well as on Meyer's website) that it is in the public domain and free to use.
 

### Normalize
Normalize is a newer approach to the CSS Reset. It is under the MIT license and documentation can be found [here.](https://github.com/necolas/normalize.css/ "GitHub Repo for Normalize")
Normalize aims to preserve useful browser defaults. It has detailed comments, normalizes styling for a wide range of elements, corrects browser bugs and inconsistencies, and can be installed with npm or yarn. 
I have included in my repo a copy of the latest normalize.css file, last updated in 2018. Of note is that some of Normalize addresses Internet Explorer, which went out of support 15 June 2022.
Normalize also makes use of many vendor prefixes.

CLI commands for yarn and npm below:

yarn
```$ yarn add normalize.css```

npm
```npm install --save normalize.css```

### Vendor Prefixes
Browsers constantly add new features. If you have questions about what does and does not require vendor prefixes, or want to test your code across browsers, I highly recommend [caniuse.com](https://caniuse.com/ "Can I Use?")
You can also check out the [GitHub Repo.](https://github.com/fyrd/caniuse "Fyrd's GitHub Repo Can I Use")

### CSS Media Queries for Breakpoints and Accessibility
A basic set of CSS media queries. Includes breakpoints for mobile, tablet, desktop, and orientation changes. At the end of the sheet media queries are listed to enable [accessibility](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_Media_Queries_for_Accessibility "MDN on Accessibility Media Queries") options for users.

### React Breakpoints

### Creating a style guide for your own projects

### Contribution Guidelines
Please see [CONTRIBUTING.md](https://github.com/mariahlaqua/Styling_Documentation/blob/main/CONTRIBUTING.md) for guidelines on adding to the project.
