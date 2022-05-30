# TAILWIND EXAMPLE

Fram Brad Traversy's YouTube video [Tailwind Crash Course | Project From Scratch](https://youtu.be/dFgzHOX84xQ).

GitHub Link: https://github.com/bradtraversy/tailwind-landing-page

**NOTE**: Great video mainly on use of the classes from header to footer and relying heaily on flexbox. He added custom color classes in the tailwind config file which I wouldn't have done. Nice hamburger menu and code except for the mobile menu positioning. I need to change that!

## Installation

- https://tailwindcss.com/docs/installation:
  - Choose **Tailwind CLI** tab
  - Install: `npm install -D tailwindcss`
  - Create **tailwind.config.js**: `npx tailwindcss init`
  - Configure your template paths: see `modules.exports` example
  - Add the Tailwind directives to your `main.css`: `@tailwind base;`, `@tailwind components;`, and `@tailwind utilities;`
  - Start the Tailwind CLI build process: `npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch` but see notes below
  - Add tailwind to your html: `<link href="/dist/output.css" rel="stylesheet">`
- use `npm watch` or `npm run watch` - stop that when you need to add npm packages, or .env files, etc

## Notes

- `npm init -y` to create package.json
- `npm i -D tailwindcss` to install as a Dependency
- `npx tailwindcss init` creates a blank default `tailwind.config.js` file
- we have to tell tailwind where to look for the utility classes
- the website has `content: ["./src/**/*.{html,js}"] ` but he is using `content: ["./*.html"]`
- he is also putting `input.css` in the root file though you can name it whatever you want - make sure to copy in the 3 directives
- you can add custom classes in that file as well and they we will compiled as well
- then run `npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch` but remove `src/`
  - but instead he is creating a script for all of that - see `package.json`
- then run `npm run build` even though there is no html file -
- run `npm run watch` then open with Live Server

### Hamburger menu

- HAMBUGER: 3 span tags inside a btn inside the main flex container - the actual hambutger menu goes just before closing nav tag
- custom css goes in index.css - the one with the directives -

## Deploy to InMotion hosting

- he has a VPS account and created a cPanel for this project...
  - options: File Manager upload, FTP, or Git Version Control
  - for Git: Create a repo > add Clone URL > then choose the path (see note below) > click Create
  - if you want to deploy to the root of your website then add the path `public_html` and of course connect your domain to your hosting account

## Git

- add `node_modules` to `.gitignore`
- if you are deploying just to host, you don't need `input.css` or `tailwind.config.js`
