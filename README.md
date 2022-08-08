# CSS_Documentation
General guidelines, for me, by me (and when noted, others), for organizing and creating CSS.

About
------
Last updated: 08/08/2022
This repo contains a set of stylesheets to be considered as a default starting point with projects. Additionally, it aims to provide insight into how to plan and execute stylesheets.
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
Browsers constantly add new features, woohoo! If you have questions about what does and does not require vendor prefixes, or want to test your code across browsers, I highly recommend [caniuse.com](https://caniuse.com/ "Can I Use?")
You can also check out the [GitHub Repo.](https://github.com/fyrd/caniuse "Fyrd's GitHub Repo Can I Use")

### CSS Breakpoints

### React Breakpoints

