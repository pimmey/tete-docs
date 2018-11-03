# Tete theme documentation
Thank you for purchasing! Feel free to contact us via item's support tab or [user's page contact form](http://themeforest.net/user/pimmey#contact).

## Installation
Installing this theme couldn't be any easier - just upload all the files to your server.

## File structure
```
| root
├── css/
├── favicons/
├── images/
├── js/
```

### root
The root contains `index.html` and all of the other directories.

### css
Your stylesheets are located under `css/` directory.

### favicons
Favicons, generated with [RealFaviconGenerator](https://realfavicongenerator.net), are located under `favicons`.

### images
Your images are located under `images/` directory.

### js
Scripts are located under `js/` directory.

## HTML structure
The theme is using the following structure:
```html
<!DOCTYPE html>
<html>
    <head>
        <!-- meta information, stylesheets, icons, title -->
    </head>
    <body>
        <canvas></canvas> <!-- magic background is located here -->
        <main>
            <!-- remaining web-site: sections, modals and footer -->
        </main>
        <!-- scripts go after the main container and just before the closing body tag -->
    </body>
</html>
```

### DOCTYPE and html tag
`<!DOCTYPE html>` is a way to declare your file as HTML5 and [`<html>`](https://developer.mozilla.org/en/docs/Web/HTML/Element/html) is the root of your document.

### head
The head tag includes a lot of important tags, like:
- [The HTML <meta> element](https://developer.mozilla.org/en/docs/Web/HTML/Element/meta) represents any metadata information that cannot be represented by one of the other HTML meta-related elements
- [The stylesheets](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/link#Including_a_stylesheet) of flexbox grid and Tete styles
- Special tags to add to the site
- The [`<title>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/title) tag

### body
Body includes all of the visible elements on your site.

## Magic background 🔮
The coolest thing about Tete is its dynamic animated background, which generates stunning abstract art.

By default, the background's config is generated randomly when the page is loaded, but you can set the values to always be the same. To do this, edit `/js/index.js` on line 60 where it says:

```js
  var CONFIG = {
    backgroundColor: BG_COLOR,
    particleNum: getRandomInt(350, 1400),
    step: getRandomInt(5, 25),
    base: getRandomInt(2000, 9000),
    zInc: getRandomArbitrary(0.0009, 0.0000009)
  };
```

Now, just above, you can see a commented out config with pretty much default values. Play around with those and save the numbers that satisfy you the most.

### Random configs
If you happen to like a random config and would like to save it, just open your [developer tools](https://developers.google.com/web/tools/chrome-devtools/) and copy the values found in console log.

## Modals
Modals are useful to display portfolio items or any other information. Tete's modals are super easy to use, just define a modal opener by adding `modal-opener` to an element's class and a `data-modal-id="my-modal"`. Then, you obviously need to create a modal element with id of `my-modal`. Feel free to add your styles or use class `modal` in order to use the predefined ones.

## Credits
### Fonts
- [Rubik](https://fonts.google.com/specimen/Rubik)

### Images
- [rawartists](https://www.flickr.com/photos/rawartists)
- [Pexels](http://pexels.com)
- [Graphic Burger](http://graphicburger.com/)

### Technologies
- [simplex-noise](https://github.com/jwagner/simplex-noise.js)
- [flexboxgrid](https://github.com/kristoferjoseph/flexboxgrid)
- [normalize.css](github.com/necolas/normalize.css)
