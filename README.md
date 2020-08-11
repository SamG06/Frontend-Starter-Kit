# Frontend-Starter-Kit 🚀 
Here are some quick start tips/resources I personally would have loved to have been aware of when I first started front-end development.

## CSS Resets
Browsers like Chrome, Firefox, Internet Explorer etc. can have different default CSS rules for certain elements. Due to this if you are not careful you can have things look good on one browser but weird on another. 

**CSS resets** help solve this problem by essentially stripping away the browsers default CSS rules so your site looks as consistent as possible across browsers. Below is what I’ve been using on my own sites recently, but you’re free to explore other CSS resets out there and use what you feel comfortable with.

🔗 - [Read this really in-depth article if you want to learn more](https://medium.com/@riittagirl/a-tale-of-css-resets-and-everything-you-need-to-know-about-them-781849d9b7f2)
```css
* {
  box-sizing: border-box;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto,
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';
  margin: 0;
  padding: 0;
  text-rendering: optimizeLegibility;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-kerning: auto;
}

:focus {
  outline: none;
}

::-moz-focus-inner {
  border: 0;
}

html {
  height: 100%;
  position: relative;
  -webkit-text-size-adjust: 100%;
}
```
