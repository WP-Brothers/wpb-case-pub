# Social Brothers WordPress Case

This is the interview case for the WordPress developer role at [WP Brothers](https://wpbrothers.nl).

This README will outline all the details and requirements of this case. Please read this document carefully before getting started.

It is important to note that the case you are about to make does not need te be perfect (or complete) when you hand it in. The purpose of this case is to see how well versed you are currently in WordPress, PHP, JavaScript(Typescript), (S)CSS and tailwind development.

We expect the case to take about 4-8 hours (depending on your level), but you can spend as much time on it as you want.

Good luck!

## Case Requirements

#### General

- Do not use any plugins
- Build upon the existing file structure and files.
- Try to write your own code as much as possible.
- We encourage writing component based code! This means reusing similar code, instead of writing the same functionality multiple times.
- Seperate presentation and logic in your code from each other as much as possible

#### Design

- Recreate the design pixel perfect as a fully working website.
- Make sure the website is fully responsive on mobile and tablet devices
  - The mobile menu must be collapsible
  - The header must be fixed on mobile

#### Scripting and styling

- Do not use jQuery. Write vanilla JavaScript or TypeScript (optional).
- Write your styling using Tailwind classes, or with SCSS/CSS using the [BEM (Block Element Modifier)](http://getbem.com/) naming methodology.
- If you are not using Tailwind, Bootstrap is available for responsive classes (see [Already Included](#already-included))).

It is important to note that the case you are about to build does not need te be perfect (or complete) when you hand it in. The purpose of this case is to see how well versed you are in WordPress, PHP, JavaScript, and (S)CSS development. Try to keep the amount of time you spend on the case under 6 hours.

## Design Specifications

You can find the design here: [Sketch Design](https://www.sketch.com/s/b8e31a79-9aa0-4c2b-8670-ad3792f01d86).

To view the technical specifications of the design, open a specific page design (for instance: Homepage), and click the button "Inspect" in the top right corner.

- The images used in the design are available in the `/assets/images` directory.
- The fonts used in the design are included in `header.php`.

## Dependencies

Before you start the case you will need to install some dependencies on your local machine.

- [Node.js](https://nodejs.org/en/) for running Yarn.
- [Yarn](https://yarnpkg.com/) for compiling local assets(Optional as npm work as well).
- [LocalWP](https://localwp.com/) for easy local WordPress development.

##### Already included:

- [Fontawesome](https://fontawesome.com/): Icon library (Free - Solid style)
- [Google Fonts](https://fonts.google.com/): Font library (Roboto and Open Sans - normal/medium/bold)
- [Tailwind](https://tailwindcss.com/): CSS framework (Enable by default, remove reference to `tailwind.css` in `src/scripts/main.ts` to disable)
- [Bootstrap](https://getbootstrap.com/): CSS framework (Disabled by default, remove comments in `src/styles/main.scss` to enable)

### Dependency Installation

#### Node.js

Node.js is a runtime environment that allows you to run JavaScript code outside of a web browser. You need it in order to run Yarn (see below).

Download the [latest installer](https://nodejs.org/en/) and follow the steps to install Node.js on your system.

#### Yarn(optional as npm can be used as well)

Yarn is a package manager for Node.js. You use it to install and run the frontend packages in your project required for asset compiling (see [Asset Compiling](#asset-compiling)). This is all done through your terminal.

Yarn can be installed through Corepack, a binary shipped with Node.js (see previous step). Execute the following terminal command:
`corepack enable`

#### LocalWP

With LocalWP it's easy to set up and manage local development environments for WordPress.This means you can run a website on a local server on your laptop, together with it's own domain name only accessible to you. When creating a new site choose the following options:

- Create a Site: `Create a new Site`
- Site name: `WPB Case`
- Environment: `Preferred`
- Username and password: `Choose yourself`
- After the installation of the local site is completed turn on One-click Admin for easy `/wp-admin` access.

## Theme development

### Theme Installation

Use the following guidelines to get started!

- Navigate to the local sites directory in your terminal. The default location of LocalWP sites is a directory calles `Local Sites`.
- Navigate to the `/themes` directory for the local site you just created.

- In the themes directory create a new folder called `wpbrothers`
- Place the contents of the entire repository (this folder) in the directory in the new theme folder

### Asset Compiling

This case template uses Webpack to bundle and compile your asset files. This means that the TypeScript and SCSS code you write is converted to .js and .css files that the browser can read and understand. Other code, like PHP and HTML, do not need to be compiled.

- This case template uses Webpack to bundle and compile TypeScript/JavaScript and SCSS.
- Write your Javascript/Typescript in /src/scripts/main.ts
- Write your CSS/SCSS in src/styles/main.scss
- The compiled assets will be placed in the `/dist` directory.

#### Install yarn packages

- Run the `yarn` of `npm install` terminal command in the `wpbrothers` theme root

After installing the dependencies you can start the development mode.

#### Development mode

While the development mode is running Webpack will watch for changes, recompile your JavaScript/TypeScript and SCSS assets and reload the server.

To start the development server:

- Run the `yarn dev` or `npm run dev` terminal command in the `wpbrothers` theme root.

You can now start writing code.

_Issues with localhost? check if your localWP site url is `wpb-case.local`_

#### Writing Code

The source files are located in `/src/`.

- The TypeScript file can be found in `/src/scripts/main.ts`
  - If you're not familiar with TypeScript you can also choose to write JavaScript. You can enable this by adding the following line above the code in `/src/scripts/main.ts` to disable the checks `// @ts-nocheck`. The compiler will then stop checking valid TypeScript and also accept valid JavaScript).
- The SCSS file can be found in `/src/styles/main.scss`
  - Tailwind is also installed so you can use that for the CSS classes if you want. The tailwind config is preset with the fonts,font-sizes and colors, in the file `tailwind.config.js` in the theme root.

The compiled assets will be placed in the `/dist` directory.

Please remember:

- Do not edit or change the files in the `/dist` folder, because they will be overwritten anytime changes from `/src` are compiled!

#### Production mode

Running Webpack in the production configuration is the last step of the development process. Running Webpack in this mode will produce optimized JS and CSS files which guarantees the best performance for your site.

To run the build process for production:

- Run the `yarn prod` of `npm run prod` command in the `wpbrothers` theme root.

Do this when you finished the case and ready to submit.

## Submitting the Case

Once you are finished with the case development, create a zip file containing the following:

- The entire `wpbrothers` theme folder
- An export of your database

Don't forget to run Webpack in the production mode before compiling your zip!

Exporting a WordPress database is very easy with LocalWP.

- Go to the 'Database' tab in LocalWP
- Click on 'Open in Adminer'
- Click on 'Export'
- Select the options:
  - output: save
  - format: sql
  - The rest can stay as is
- Make sure all database tables are selected
- Add the `.sql` file to your theme files

Thank you for showing interest in our company and taking the time to make this case. We hope to speak with you soon!
