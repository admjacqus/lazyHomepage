# Lazy Homepage

Missguided homepage, boosted performance using lazySizes.

## Getting Started

These instructions will get you a copy of the homepage up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the homepages on Magento.

### Installing

You will need Node.js for this step.

```bash
# clone the repo
$ git clone

# install NPM dependencies
$ npm install

# start gulp & browsersync
$ npm start
```

## Project structure

```
├── css
|  ├── slick-theme.css
|  └── style.css
├── index.html
├── js
|  └── index.js
├── sass
|  └── style.scss
├── views
|  └── your-html.html
├── base-2.css
├── base.css
├── gulpfile.js
├── index.html
├── layout.xml
├── main.css
├── main.js
├── package.json
└── README.md
```

## Process

```bash
# start gulp & browsersync
$ npm start
```

Amend any of the SCSS, HTML or JS files and see the browser update with your changes live in browser.

## Amending styles

Most styles within a homepage will be added inline atop the homepage, or even better, inline in styleblocks within the elements div.
_See 'your-html.html line 3 and 72'_

There are a few style blocks in the project, with a hierachy, so it's important to know what's what.

```
├── base-2.css
├── base.css
```

These styles are lifted from the live homepage, we do not maintain this code, but it is neccesary to create an accurate local homepage. Leave it!

```
├── css
|  └──  slick-theme.css
```

These come from Slick, they are not used in the current project, but come in handy for testing. No need to maintain.

```
├── css
|  └── style.css
├── sass
|  └── style.scss
```

These are our styles, we have created these and maintain the code but, as they are just base styles, therefore are not updated regularly. They are hosted on the server, and inserted into the live page using a link (see index.html line 2) to aid in caching etc.

If you do amend this code, we would need to replace the file on the server. Email adam.jacques@missguided.com.

## Deployment

Code good to go? OK, copy all the code within _your-html.html_ and paste into the 'Content' tab of the CMS page on Magento.

See _layout.xml_ for necceasry code to be inserted within **Design > Layout Update XML**

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
