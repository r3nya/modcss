Modular CSS Experiment
======================

0: Basics
---------

* `npm run serve`: **Run a local dev server on port 8888.** (Depends on
    [local-web-server](https://www.npmjs.com/package/local-web-server), a simple web-server
    for productive front-end development.)
* `js:bundle`: **Build a JS bundle.** (Depends on
    [requirejs](https://www.npmjs.com/package/requirejs), the node adapter for RequireJS,
    for loading AMD modules. Includes the RequireJS optimizer.)
* `css:bundle`: **Build a CSS bundle.** (Depends on
    [node-sass](https://www.npmjs.com/package/node-sass), the node bindings for the Sass
    stylesheet preprocessor.) This will transpile all the `*.scss` files in our project and output
    a `bundle.css` at the root of our app - which is the (one-and-only) CSS file referenced in
    `index.html`. Note that `css:bundle` relies on `style/style.scss` to 'know' which `.scss` files
    to bundle. We need to maintain `style/style.scss` as we add/remove/relocate `.scss` files.
* `css:bundle-when-styles-change`: **Watch for style changes and rebuild CSS bundle in response.**
    (Depends on [node-sass](https://www.npmjs.com/package/node-sass) and
    [onchange](https://www.npmjs.com/package/onchange). The latter module facilitates the use of
    glob patterns to watch file sets and run commands when anything is added, changed or deleted.)
