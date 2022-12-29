# Styling Documentation


About
------
#### This is a work in progress.
This repo contains a set of documents & links to be considered as a default starting point for styling projects. These are general guidelines for organizing, creating and making styling decisions. Especially geared towards web developers working on hobby or personal projects who already have a fundamental understanding of CSS, js, React, etc. This does not include information specific to mobile dev, such as Flutter & React Native. 

Additionally, it aims to provide insight into how to plan and execute styling.  Empty sections indicate where resources are still being gathered.
Hopefully this planning allows for greater ease when planning and returning returning to projects after some time away from them. It also aims to aid in planning collaborative efforts.

Planning
------

### Creating a style guide & wireframe for your project
This can be referred back to and (at least for me) is easier to read then digging through a CSS file. There are free style guide and wireframe templates available on [Figma](https://www.figma.com/). I love this style guide template from [Valeriya Desire.](https://www.figma.com/community/file/1000026521402926606 "Style Guide UI Kit on Figma") It can be a great starting point to make your own. Once you make one style guide it can be easily recycled and updated for each project.

If you are new to Figma, [this 45minute tutorial](https://www.youtube.com/watch?v=m0sHva0JjZE&t=17s&ab_channel=AdrianTwarog) from Adrian Twarog shows a UI designer's Figma work flow for a single page website wireframe.

### Illustrations, Icons & Fonts

[unDraw](https://undraw.co/license) is a collection of illustrations that are generally free to use. If you plan on monetizing your project please read the license carefully.

[Font Awesome](https://fontawesome.com/) is a collection of icons. There are enough free icons to cover most needs.

[fontpair](https://www.fontpair.co/all) has a collection of [Google Fonts](https://fonts.google.com/) pre-paired together. You will need to pull the code from Google.

[Google Icons:](https://fonts.google.com/icons) Google's collection of UI icons.

### Documenting Your Own Projects
Basic ideas to preserve sanity:
* Separate purpose by file (when it makes sense)
* Name things in a way that makes sense.
* Divide things into [logical sections](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Organizing "MDN: Organizing Your CSS")
* For files that become very long, see first item, or, create a table of contents at the beginning.
* Write detailed comments


CSS Stylesheets
------
Starting with basic, older stylesheets and up to Materialize UI.

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


### CSS Media Queries for Breakpoints and Accessibility
A basic set of CSS media queries. Includes breakpoints for mobile, tablet, desktop, and orientation changes. At the end of the sheet media queries are listed to enable [accessibility](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries/Using_Media_Queries_for_Accessibility "MDN on Accessibility Media Queries") options for users.

Considerations, Flexbox & Grid cheatsheets & alternative styling methods
------

### Vendor Prefixes
Browsers constantly add new features. If you have questions about what does and does not require vendor prefixes, or want to test your code across browsers, I highly recommend [caniuse.com](https://caniuse.com/ "Can I Use?")
You can also check out the [GitHub Repo.](https://github.com/fyrd/caniuse "Fyrd's GitHub Repo Can I Use")

### Flexbox and Grid
[Grid cheatsheet from Malven Co.](https://grid.malven.co/ "Grid Cheatsheet")

### Materialize UI
Materialize UI will do much of the heavy lifting for you. It has built in break points and is built by Google's Material Design team. You can use [cdnjs.com](https://cdnjs.com/libraries/materialize) to link the stylesheet, or [download different versions of it](https://materializecss.com/) to include in projects. [The github repository](https://github.com/Dogfalo/materialize). There is excellent documentation available.

CLI for npm
```npm install materialize-css@next```

Styling React
------
[Material UI, MUI, can be used with React.](https://mui.com/material-ui/getting-started/overview/) This provides an entire library of components, icons, etc. that can be imported as needed for use with a project. There are several variations, but the standard, and free, Emotion styling package can be installed with the following commands:

Install library

```npm install @mui/material @emotion/react @emotion/styled```

```yarn add @mui/material @emotion/react @emotion/styled```

Install Roboto Font from Google Fonts

```npm install @fontsource/roboto```

```yarn add @fontsource/roboto```


Install MUI Icons

```npm install @mui/icons-material```

```yarn add @mui/icons-material```

It is also possible to install with the CDN - but installing the package and importing what is needed will result in improved performance.


## Tailwind CSS and Controlling className in Create-React-App

Some packages that can be used to work with [Tailwind CSS](https://tailwindcss.com/docs/guides/create-react-app) include: [classnames](https://www.npmjs.com/package/classnames) and [prop-types](https://www.npmjs.com/package/prop-types). These allow the creation of one component with many styling options, based on the props passed into the component at rendering. For example, you may want a button with primary, secondary, warning, success, outline, and rounded variations. These variations can be controlled with boolean props, where the prop is present or it is not. PropTypes can throw an error when duplicate styling props are passed into a component. classnames can create the string to be entered into the components className attribute based on the props. Note that TypeScript has built in prop validation and so prop-types is not necessary.

Here's the general installation procedures for these when create-react-app is already installed, from the app directory:

```npm install -D tailwindcss```

```npx tailwindcss init```

```npm install prop-types```

```npm install classnames```

To configure Tailwind CSS, open the ```tailwind.config.js``` file and replace the content section configuration:

```
module.exports = {
  content: [
    "./src/**/*.{js,jsx,ts,tsx}",
  ],  
 ```

Change directory to the src folder, and create an ```index.css``` file. Inside this file paste the following:

```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

Finally, make sure to import the css to your ```index.js``` file in the src directory:

```import './index.css';```

Further documentation on prop-types and classnames can be found by clicking the links provided above.

### Contribution Guidelines
Please see [CONTRIBUTING.md](https://github.com/mariahlaqua/Styling_Documentation/blob/main/CONTRIBUTING.md) for guidelines on adding to this project.
