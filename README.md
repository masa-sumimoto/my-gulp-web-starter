# My Gulp Web Site Starter
This is my starter kid for creating website with Gulp. :full_moon_with_face:


## About This Environment
The following list is an introduction to the modules in this environment.

```
Core:
Node Packages Management => Yarn
Task Runner / Module bundler => Gulp4 & Webpack4
Command Line Utility => minimist
Automatic Browser Loading => browserSync

for Javascript:
Transpiler => Babel
Linter => ESLint
Cording Library => jQuery

for Style:
Utility => gulp-postcss / gulp-sass / Autprefixer
Linter => stylelint
CordingLibrary => Bootstrap4

for Images:
Minify => imagemin ( and imagemin plugins )

for HTML:
Minify => gulp-htmlmin

and many other packages. Thanks.
```


## What Can You do with this Kid?
- You can start html cording quickly.
- You can get a browser reload every time you make a change to your code.
- You can use JavaScript ES6 Way.
- You can use SCSS as style meta language.
- You can get minified HTML sources.
- You can get compiled ES5 JavaScript sources.
- You can get compiled styles that contains styles with backward compatibility.
- You can get an automatically compressed images.
- You can separate and manage images that you do not want to compress and images that you want to automatically compress.
- You can also get webP images automatically.


## How to Use the environment

### Prerequisites
- Command line operation.
- To be installed node.js on your PC.
- To be installed yarn on your PC.

### Installation
You can start coding immediately in the following way.

1. Clone this repository: `git clone git@github.com:sumi37/gulp-web-site-starter.git` (or download)
2. Move directory: `cd gulp-web-site-starter`
3. Install node modules with yarn: `yarn install`
4. Start server: `yarn run serve`
5. View the site at `http://localhost:8080/`
6. Reload the page. (First time only)

※ If you want to stop server, Please use `ctrl+c` on your shell.


## About Editing Methods

### About Build
You need to edit files in `./src/*`.  
The files will be compiled as `dest/*`.  
While running the server, you can get compiled files for each save edit files.
Also, if you change the server startup method from `yarn run serve` to `yarn run serve --production`, you can get the minified styles and scripts for production.

You also can use `yarn run build` and `yarn run build --productioon` commands.  
These only compile. The server does not start.

### About Scripts
You need to save scripts to `./src/assets/javascripts/**/*.js`.  
The files will be compiled as `dest/assets/javascripts/bundle.js`.  
You can use ES6 and ES5 style. the scripts will be compiled as ES5.  
If you want to know the corresponding browser version, Please look `.browserlistrc`.

### About Styles
You need to save styles to `./src/assets/stylesheets/**/*.scss`.  
The files will be compiled as `dest/assets/stylesheets/bundle.scss`.  
This environment is intended to create web pages, and may not be suitable for creating web applications.
As a reason, the style is divided in the website specific context.

The following is the context of the style I suggest.  
`Core`, `Libralies`, `Layouts`, `Complex Parts`, `Primitive Parts`, `Pages` and `User`  
The sass stylesheets are defined accordingly.  

I also use Bootstrap a lot and prefer styles that override it.
If you don't like the style, Please remove styles in `src/assets/[dirname]/*.scss` and remove import lines of `src/assets/application.scss`. Design is possible in your style.

## About Images
You need to save images to `src/assets/images/**/*.{png, jpg, svg, gif}`.  
The files will be compiled as `dest/assets/images/**/*.{png, jpg, svg, gif}`.  
Your images are compressed automatically. ( and If your image is `jpg` or `png`, You can also get `webp` image. )  
If you don't want to compress images, Please add `__` to image name as prefix. like `__foo.png`. The image is not compressed.
