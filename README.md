# Quidax Book Club

## Front-end Engineer Skill Assessment

Implementating a dashboard view for the fictional Quidax Book Club web application using HTML, CSS/SCSS, vanilla Javascript, and ​only​ the suggested libraries/plugins for certain UI elements.

## Commands

After you clone this project, these commands are available in `package.json`.

```bash
yarn run dev # run the app in development mode
yarn run watch:sass # watches for changes in sass files, converts scss files into CSS and auto-compiles Sass every time changes are made.
yarn run build:css # compiles, prefixes and compresses sass files to a single style.css file.
yarn run format # format source files with Prettier
```

## Playing locally

First, you will need to install [NodeJS](https://www.nodejs.org/) or [Yarn](https://www.yarnpkg.com) on your machine.

After installing, navigate to the project root folder and install it's dependencies.

```bash
$ yarn install
```

Then, run the web app in development mode.

```bash
$ yarn run dev

[0] Serving "/Users/dr_hemm/Documents/Projects/quidax-engineering-ui-assessment" at http://127.0.0.1:8080
[0] Ready for changes
```

> Note that the server may start on a different port if :8080 is in use.

## Directory structure

### Overview

```tree
├─css/
│  ├─ style.comp.css
│  ├─ style.css
│  ├─ style.prefix.css
├─ js/
│  ├─ index.js
├─ sass/
|  ├─ abstracts/
|  |  ├─ _mixins.scss
|  |  ├─ _overrides.scss
|  |  ├─ _variables.scss
│  ├─ base/
|  |  ├─ _animations.scss
|  |  ├─ _base.scss
|  |  ├─ _typography_.scss
|  |  ├─ _utility.scss
│  ├─ components/
|  |  ├─ _badge.scss
|  |  ├─ _book-card.scss
|  |  ├─ _book.scss
|  |  ├─ _rating.scss
│  ├─ layout/
|  |  ├─ _footer.scss
|  |  ├─ _header.scss
|  |  ├─ _navbar.scss
│  ├─ pages/
|  |  ├─ _dashboard.scss
│  └─ main.scss
├─ index.html
├─ package.json
└─ README.md
```

### css/

Here is where the styles are compiled to.

### js/

All JavaScript files are stored here.

#### js/index.js

UI logic is implemented here.

### sass/

Sass stylesheets are in this folder.

#### sass/main.scss

This is the main entry point for all Sass files.

### index.html

The app's main entry point.

## Issues faced

### Cross-browser compatibility

The scrolling momentum on fixed containers worked as expected on desktop browsers, but didn't work on touch devices, especially iOS browsers

#### Fix

Set -webkit-overflow-scrolling property of parent container to touch.

> Line 74: '/sass/base/_base.scss'

```css
-webkit-overflow-scrolling: touch;
```

## Feedback

Duplicating DOM elements and populating them with random data causes an unnecessary increase in development time. Though it's not difficult or stressful, it would be better if candidates could dynamically populate the DOM.

An API or a JSON file that provides data about these books would be ideal.

It would reduce development time and also give you (the recruiter) more insight to the candidates' technical skills.
