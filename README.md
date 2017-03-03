# Yao Boilerplate
A simple PostCSS boilerplate built using npm scripts

## Features

- Light NPM Build Tool
- PostCSS (minimal plugins - targeting consistency with CSS4)
- Autoprefixer
- BEM Naming Conventions
- CSS/JS Minification
- CSS/JS Source Mapping
- Image Minification/Optimization

## Get Started

Clone the repository

``` bash
git clone https://github.com/wad3g/yao-boilerplate.git
cd yao-boilerplate
```

Install the dependencies.

``` bash
npm i
```

Start watching files for compilation.

``` bash
npm start
```

## Scripts

*Yao Boilerplate* uses npm scripts as the _only_ build tool. Here's a list of available tasks:

#### `npm start`

Spin up a dev server of your app and compiles `/src/css/app.css` to `/dist/css/app.css`. The app should automatically launch in your browser. If you use a different dev server, the default / 404 route should be configured to `index.html`. Runs the `http-server`, `livereload`, `opener` and `watch` commands, which should automattically launch the app in your browser and watches for any changes in the `dist/` directory.

The `watch` command keeps multiple processes running at one timing by using [Parallelshell](https://www.npmjs.org/package/parallelshell). This means when a change is detected on one of your processes _only_ that process will recompile -- not the entire app.

#### `npm run build`

Only compiles the `/src/css/app.css` file and outputs to `/dist/css/app.css` without watching the file tree.

#### `npm run minify`

Uses [cssano](http://cssnano.co/) and [imagemin-cli](https://github.com/imagemin/imagemin-cli) to minify/optimize your CSS and images. You can run these tasks individually using `npm run minify:css` or `npm run minify:img`.

#### `npm run clean`

Delete `rm -vrf dist/*`  all existing `dist/` files.

#### `npm run watch`

Uses the following tasks, `watch:html`, `watch:css`, and `watch:img`, to watch for changes in `src/`, then recompile the changes to the `dist/` directory.

#### `npm run autoprefixer`

Adds vendor prefixes to your compiled CSS automattically

#### `npm run sourcemaps`

Generate sourcemaps.

## Technologies
The boilerplate uses some of the following PostCSS plugins, npm scripts, and commandline tools:
- [x] [http-server](https://github.com/indexzero/http-server)
- [x] [imagemin-cli](https://github.com/imagemin/imagemin-cli)
- [x] [live-reload](https://github.com/Raynos/live-reload)
- [x] [onchange](https://github.com/Qard/onchange)
- [x] [opener](https://github.com/domenic/opener)
- [x] [Parallelshell](https://www.npmjs.org/package/parallelshell)

### PostCSS Plugins
- [x] [autoprefixer](https://github.com/postcss/autoprefixer): Automatically adds vendor prefixes
- [x] [cssano](http://cssnano.co/): Minify and optimize CSS
- [x] [postcss-cli](https://github.com/postcss/postcss-cli): CLI for PostCSS
- [x] [postcss-color-function](https://github.com/postcss/postcss-color-function): Transform W3C CSS color function to more compatible CSS
- [x] [postcss-comment](https://github.com/zoubin/postcss-comment): Allow support for inline comments
- [x] [postcss-custom-properties](https://github.com/postcss/postcss-custom-properties): Transform W3C CSS Custom Properties for cascading variables
- [x] [postcss-import](https://github.com/postcss/postcss-import): PostCSS plugin to inline `@import` rules content
- [x] [postcss-media-variables](https://github.com/WolfgangKluge/postcss-media-variables): Use CSS Custom Properties in media query parameters
- [x] [postcss-nested](https://github.com/postcss/postcss-nested): Unwrap nested rules like SASS
- [x] [postcss-mixins](https://github.com/postcss/postcss-mixins): Traditional pre-processor style mixins
