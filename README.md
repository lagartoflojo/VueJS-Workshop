# Gulp-Boilerplates
<p align="center">
  <a href="https://raw.githubusercontent.com/CKGrafico/Gulp-Boilerplates/master/LICENSE">
    <img src="https://img.shields.io/badge/license-MIT-blue.svg"
         alt="license">
  </a>

  <a href="https://codeclimate.com/github/CKGrafico/Gulp-Boilerplates">
    <img src="https://codeclimate.com/github/CKGrafico/Gulp-Boilerplates/badges/gpa.svg" 
        alt="codeclimate"/>
  </a>
</p>

## Quickstart
On this repo you can find some boilerplates based on Gulp, each branch has a different example.
We try not only to use Gulp, also to use best practises and real examples that we can use on real projects.
- **[master](https://github.com/CKGrafico/Gulp-Boilerplates/tree/master):** Stable version of a basic and generic example.
- **[dev](https://github.com/CKGrafico/Gulp-Boilerplates/tree/dev):** Dev version of a TypeScript example.
- **[ts-master](https://github.com/CKGrafico/Gulp-Boilerplates/tree/ts-master):** Stable version of a TypeScript example.
- **[ts-dev](https://github.com/CKGrafico/Gulp-Boilerplates/tree/ts-dev):** Dev version of a basic and generic example.
- **[node-ts-master](https://github.com/CKGrafico/Gulp-Boilerplates/tree/node-ts-master):** Stable version of node-based with TypeScript example.
- **[node-ts-dev](https://github.com/CKGrafico/Gulp-Boilerplates/tree/node-ts-dev):** Dev version of node-based with TypeScript example.
- **[vue-master](https://github.com/CKGrafico/Gulp-Boilerplates/tree/vue-master):** Stable version of vue-based example. 
- **[vue-dev](https://github.com/CKGrafico/Gulp-Boilerplates/tree/vue-dev):** Dev version of vue-based example.
- **ng2-master:** Stable version of angular2-based example. [To do]
- **ng2-dev:** Dev version of angular2-based example.

## Table of Contents
  1. [App Technologies](#app-technologies)
  1. [Tasks Technologies](#task-technologies)
  1. [Running tasks](#running-tasks)
  1. [Environments](#environments)
  1. [Project structure](#project-structure)
  1. [Gulpfile](#gulpfile)
  1. [Gulpfile Helpers](#gulpfile-helpers)
  1. [Gulpfile Paths](#gulpfile-paths)
  1. [Contributors](#contributors)
  1. [License](#license)

## App Technologies
On this branch _(Basic)_ we use:
- **BEM + BEMIT + etc:** A mix of BEM and related-BEM technologies to create conventions for CSS classes.
- **TypeScript:** All the code uses TypeScript.
- **jQuery:** Only to show how to import an external library.
- **Linting:** Linting for TypeScript and SASS.
- **Normalize:** Normalize our css, you can extend it easily.
- **SASS:** Scss structure with good practises.

**[ back to top](#table-of-contents)**

## Tasks Technologies
On this branch _(Basic)_ we use:
- **Concurrently:** Execute two tasks in parallel.
- **Gulp Autoprefixer:** Add browser prefixes for last two versions of the browsers.
- **Gulp Clean CSS:** To minify CSS.
- **Gulp Connect:** Preview website on local server.
- **Gulp Environment:** Call to different tasks depending of the environment.
- **Gulp Fontmin:** Generate fonts from .ttf.
- **Gulp Imagemin:** Compress images.
- **Gulp Load plugins:** Load all the plugins once.
- **Gulp Newer:** On some tasks we want to do something only with the newer files.
- **Gulp Noop:** Basic Noop but on stream.
- **Gulp Sass:** Compile Scss to CSS.
- **Gulp Sasslint:** Linting for SASS.
- **Gulp Sourcemaps:** Generate Sourcemaps when is necessary.
- **Opn:** Open browser to see the preview.
- **Require all:** Load all gulp tasks once.
- **Webpack and Babel:** To use Babel with Webpack _(TypeScript -> ES5)_ and create a bundle.
- **Webpack and Linting:** To check TypeScript files.

**[ back to top](#table-of-contents)**

## Running tasks
To run the tasks we have these three commands:
- Install dependencies:
> npm install

- Running tasks on production mode:
> npm run prod

- Running tasks on development mode:
> npm run dev

- Running tasks on local mode:
> npm run local

- Running tasks on watch mode and serve the app:
> npm start

**[ back to top](#table-of-contents)**

## Environments
On this project we have two environments:
- **Local:** Use this on your computer
- **Development:** Use this on your dev server
- **Production:** Use this on your production server

## Project structure
On this branch _(Basic)_ the structure is:`
```
./
│
├── app/
│   ├── assets/
│   │   ├── fonts/
│   │   │   └── OpenSans
│   │   │       ├── OpenSans-Regular.ttf
│   │   │       ├── ...
│   │   │       └── OpenSans-SemiboldItalic.ttf
│   │   │
│   │   └── images/
│   │       └── example.jpg
│   │
│   ├── scripts/
│   │   └── app.ts
│   │   └── vendor.ts
│   │
│   └── styles/
│       ├── base/
│       │   ├──  mixins # Some mixins to use on base folder
│       │   ├── _fonts.scss # Load the fonts for your project
│       │   ├── _globals.scss # Global styles
│       │   ├── _states.scss # States classes, like is-hidden, is-visible...
│       │   ├── _utilities.scss # Utility classes, like u-mt-10@xs _(margin-top 10px on media screen xs)_
│       │   └── _variables.scss # Global variables of the project
│       │
│       ├── components/
│       │   └── _ck-site.scss # Example of BEM based component
│       │
│       ├── vendor/
│       │  └── _normalize.scss # Import and extend Normalize
│       │
│       └── index.html
│
├── dist/ # Distribution folder
│
├── tasks/ # Gulp tasks
│   ├── config/
│   │   ├── helpers.js # Helpers that useful for tasks
│   │   └── options.js # Internal operation to use with tasks
│   ├── rules/
│   │   ├── scripts.js # Create a bundle for TypeScript files
│   │   └── scripts-lint.js # Check linting of TypeScript files
│   ├── assets.js # Minify images and generate fonts
│   ├── clean.js # Clean distribution folder
│   ├── copy.js # Copy index.html to dist
│   ├── serve.js # Open a browser with the preview of the project
│   ├── styles.js # Compile and compress SASS files when is necessary
│   ├── styles-lint.js # Linting for SASS
│   └── watch.js # Watcher for files
│
├── .gulpenvrc.yml # Environments configuration
├── .sass-lint.yml # SASS linting configuration
├── .scripts-lint.json # TypeScript linting configuration
├── gulpfile.js # Main gulp file
├── package.json # Configure npm tasks and dependencies
├── tasks.config.json # Configure paths and options for tasks
└── webpack.config.js # The Webpack configuration for scripts
```

**[ back to top](#table-of-contents)**

## Gulpfile
This is how we configured the main file:
```
// We load all the tasks and pass some parameters
let tasks = require('require.all')('./tasks');
tasks((name, task) => { func = () => task(gulp, paths, $, _, tasks); func.displayName = name; return func});
// paths is for all the project paths
// $ is for plugins
// _ is for helpers
```

And these are the only two tasks:
```
gulp.task('default', gulp.series(tasks.clean, tasks.stylesLint, tasks.styles, tasks.copy, tasks.assets));
gulp.task('watcher', gulp.parallel(tasks.serve, tasks.watch));
```

**[ back to top](#table-of-contents)**

## Gulpfile Helpers
In case that you want to modify some gulp tasks, this helpers can help you.

- Files and folders:

```
_.folder(paths.app.scripts);
```
Returns the path where the scripts are located, example: _'./app/js/'_

```
_.files(paths.app.scripts)
```
Returns the file pattern to get the scripts, example: _'./app/js/**/*.js'_

```
_.files(paths.app.scripts, _.NOT)
```
Exclude scripts, example: _'!./app/js/**/*.js'_

```
_.abs(_.folder(paths.app.scripts), __dirname)
```
Change path to absolute path: _'C:/project/app/js'_

**[ back to top](#table-of-contents)**

## Tasks configuration
You can configure different things related with the tasks.
```
{
    "app": {
        "assets": {
            "images": {}
        }
    }
};
```
You can acces to files and folders like:
```
_.folder(paths.assets.images);
// ./app/assets/images/

_.files(paths.assets.images)
// ./app/assets/images/**/*.*
```

But you can extend this structure:

```
{
    "app": {
        "assets": {
            "images": {},
            "fonts": {
                "files": "**/*.ttf",
                "folder": "custom"
            }
        }
    }
};
```
You can acces to files and folders like:
```
_.folder(paths.assets.fonts);
// ./app/assets/custom/

_.files(paths.assets.fonts)
// ./app/assets/custom/**/*.ttf
```

Also you can use the parent folder

```
{
    "app": {
        "assets": {
            "images": {},
            "fonts": {
                "files": "**/*.ttf",
                "folder": "custom"
                "roboto": {
                    "files": "Roboto.ttf",
                    "folder": "..",
                }
            }
        }
    }
};
```
And the result will look like that:
```
_.folder(paths.assets.fonts.roboto);
// ./app/assets/fonts/

_.files(paths.assets.fonts.roboto)
// ./app/assets/fonts/roboto.ttf
```

**[ back to top](#table-of-contents)**

## Contributors

[View Contributors](https://github.com/CKGrafico/Gulp-Boilerplates/graphs/contributors)

## License

(The MIT License)

Copyright (c) 2014-2017 Airbnb

Permission is hereby granted, free of charge, to any person obtaining
a copy of this software and associated documentation files (the
'Software'), to deal in the Software without restriction, including
without limitation the rights to use, copy, modify, merge, publish,
distribute, sublicense, and/or sell copies of the Software, and to
permit persons to whom the Software is furnished to do so, subject to
the following conditions:

The above copyright notice and this permission notice shall be
included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED 'AS IS', WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY
CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT,
TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

**[ back to top](#table-of-contents)**