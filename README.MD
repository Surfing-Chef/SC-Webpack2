# Webpack 2 Tutorials #
This repository holds the source code of Webpack 2 Tutorials. Each branch is a separate Webpack set-up.  Each has been authored based on a separate tutorial.  

- **[WEBPACK HOMEPAGE](https://webpack.github.io/docs/)**
- **[WEBPACK 2 HOMEPAGE](https://webpack.js.org/)**


## Webpack 2 Basics ##
- [7 video series](https://www.youtube.com/playlist?list=PL55RiY5tL51rcCnrOrZixuOsZhAHHy6os) on YouTube
- The full source code can be found in the following Github repo (choose the right branch!): https://github.com/mschwarzmueller/yt-webpack2-basics

### Core Concepts ###
Four core concepts Webpack is based on:  
1. **Entry** - Where should Webpack start looking for dependencies and what to bundle. The entry point is the contextual root or the first file to kick off your app. There may be one or many.  
2. **Module Loaders** - Transformations that are applied on a resource file - source code of a module of your app. They are functions (running in node.js) that take the source of a resource file as the parameter and return the new source, that is they allow you to pre-process files as you import or "load" them. ([webpack.github.io](https://webpack.js.org/concepts/loaders/))
3. **Plugins** - Add functionality typically related to bundles in webpack ([webpack.github.io](https://webpack.github.io/docs/using-plugins.html) and [webpack.js.org](https://webpack.js.org/concepts/plugins/))
4. **Output** - Where Webpack stores the bundle or bundles. One for each entry point.

### Config File ###
Webpack's configuration file is a JavaScript file that exports an object. This object is then processed by webpack based upon its defined properties.([Configuration](https://webpack.js.org/concepts/configuration/))
