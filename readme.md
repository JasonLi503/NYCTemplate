# NYUAD Public Website Front End


This template is based on the official ZURB Template for use with [Foundation for Sites](http://foundation.zurb.com/sites). It has a Gulp-powered build system with these features:

- Handlebars HTML templates with Panini
- Sass compilation and prefixing
- JavaScript concatenation
- Built-in BrowserSync server  (Which will open the default page in browser upon the start in the localhost:8000)
- For production builds (not necessarily we'll use this, but still included):
  - CSS compression
  - JavaScript compression
  - Image compression

## Installation

To use this template, your computer needs:

- [NodeJS](https://nodejs.org/en/) (0.12 or greater)
- [Git](https://git-scm.com/)


### Setup

To manually set up the template, first download it with Git:


Unzip the packaged boilerplate file you've downloaded.Open the folder in your command line, and install the needed dependencies:

```bash
cd projectname
npm install
bower install
```

Finally, run `npm start` to run Gulp. Your finished site will be created in a folder called `dist`, viewable at this URL:

```
http://localhost:8000
```
To create compressed, production-ready assets, run `npm run build`.

'dist' folder is where all the compiled HTML, CSS and JS files will reside. This folder removed and recreated every time the we run the `npm start` command.

### Templating Guide (Panini)
Each component will be created in a separate html document and placed inside the `src/partials` folder (ex. `header.html`). The actual templates will be created in the `src/pages/templates` folder (ex. `template-type1.html`). In the template any component can be called like this `{{>component_name}}`  for example the header component will be called `{{>header}}` without *.html* extension. 
 
 Once compiled the same template file (ex. **template-type1.html**) will be generated in the `dist\templates\` folder with the same name. This will have all the html components with correct indentions etc. in a full page. 
 
 #### Compiled CSS and JavaScript
 
All the SASS files will be placed in the `src\assets\scss` folder in the respective component name. (ex **_footer.scss**) which will be compiled in to **base.css** and placed in the `dist\assets\css` folder.

Same goes with JS files too. All the files placed in to `src\assets\js` will be compiled / concatenated  in to one single **scripts.js** file and placed in the `dist\assets\js` folder.


### Viewing the template files in the browser
To view the template files in the browser, please use `http://localhost:8000/templates/<<template_file_name>>` format. For instance to view the *template-1-3-1.html* template, go to `http://localhost:8000/templates/template-type1.html`. By default browserSync is configured to load the  `template-1-3-1.html` file to the browser when you run the `npm start` command.