# Webpack 2 Tutorials #
This repository holds the source code of Webpack 2 Tutorials. Each branch is a separate Webpack set-up.  Each has been authored based on a separate tutorial.  

- **[WEBPACK HOMEPAGE](https://webpack.github.io/docs/)**
- **[WEBPACK 2 HOMEPAGE](https://webpack.js.org/)**


## Webpack 2 Basics ##
- [7 video series](https://www.youtube.com/playlist?list=PL55RiY5tL51rcCnrOrZixuOsZhAHHy6os) on YouTube
- The full source code can be found in the following Github repo (choose the right branch!): https://github.com/mschwarzmueller/yt-webpack2-basics

### HTML + Image Loaders ###
This workflow builds on a Babel + SCSS Workflow.

Files are arranged in src and dist folders.  All working assets and files used to create the project are organized in the src folder: SASS, JS, HTML, img, etc. The dist folder is the output destination, organizing all the processed assets necessary for a complete deployment package, all in one folder.

This workflow will inject CSS and JS links into the HTML file automatically. It will also copy required image files from the src folder into the dist folder.

This workflow uses 2 processes SCSS and JS.
All the imports terminate in app.js, but the css or scss doesn't get mixed with the javascript. Webkit just starts its journey there.
#### SASS ####
1. *main.scss* imports *\_color.scss*
2. **sass-loader** compiles scss to css
3. **css-loader** allows js to handle css
4. Rather than **style-loader** injecting the css into the head of out html page, use **ExtractTextPlugin** to extract css to its own file - *main.css*

#### JS ####
1. *app.js* imports *random-generator.js*
2. **babel-loader** uses the **ES2015 preset** plugin to transpile ES6 to ES5
3. Exports processed file as *app.bundle.js*

#### HTML ####
In the head of *index.html*, a link to *main.css* imports the styles, while a script tag just before the closing body tag imports the *app.bundle.js* js file. Both files were processed into the *dist* folder specified in the output of the  *webpack.config.js* file.  The **webpack-dev-server** node package will auto load updates during developments, and stores the files it uses in memory.

#### USAGE ####
The package.json file specifies a development script and a production script:
```console
# development
> > npm run build  

# production
> npm run build:prod      
```
