# Lazy Homepage

Missguided homepage, boosted performance using lazySizes.

## updates [22/03]

```diff
+ //these elements have been redacted
- .imgContainer
- .title-below
```

## Getting Started

These instructions will get you a copy of the homepage up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the homepages on Magento.

---

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

---

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
├── main.js
├── package.json
└── README.md
```

### files and what they do.

* `base*.css` both stylesheets are lifted from Magento and not maintained by us.
* `style.scss` These are our styles, we have created these and maintain the code but, as they are just base styles, therefore are not updated regularly. They are compliled into `css/style.css` on save. This stylehseet is hosted on the server, therefore, any amends to this would require uploading/replacing

```
//static.missguided.co.uk/media/upload/HOMEPAGE/lazy/style.css
```

* `index.html` is a replica of the magento wrapper, and includes scripts & stylesheets just like the real thing.
* `your-html.html` is where our custom code is added, this is injected into `index.html` on line 384.
* `main.js` injects `your-html.html` into `index.html` on load.

---

## Process

```bash
# start gulp & browsersync
$ npm start
```

Amend any of the SCSS, HTML or JS files and see the browser update with your changes live in browser.

---

## Amending styles

### Amending _style.scss_

Please see _Project structure/files and what they do_.

To see amends live in the browser, you will need to comment out the link and un-comment the link to our local, compiled stylesheet. Please be aware any amends would need to be uploaded/replaced on the server.

```html
<link rel="stylesheet" href="css/style.css">
<!-- <link rel="stylesheet" type="text/css" href="//static.missguided.co.uk/media/upload/HOMEPAGE/lazy/stylesheet.css"> -->
```

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

If you do amend this code, we would need to replace the file on the server. Email adam.jacques@missguided.com.

---

## Deployment

Code good to go? OK, copy all the code within _your-html.html_ and paste into the 'Content' tab of the CMS page on Magento.

See _layout.xml_ for necceasry code to be inserted within **Design > Layout Update XML**

---

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
