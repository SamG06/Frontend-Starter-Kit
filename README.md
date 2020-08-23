# Frontend-Starter-Kit (WIP) 🚀 
Here are some quick start tips/resources I personally wish I had been aware of when I first started my journey into the world of front-end development. I am assuming you already know the basics and made a simple project or two. If you are an absolute beginner I go more in depth of how to get started from zero in my blog post here.


## CSS Resets

Browsers like Chrome, Firefox, Internet Explorer etc. can have different default CSS rules for certain elements. Due to this if you are not careful you can have things look good on one browser but weird on another. 

**CSS resets** help solve this problem by essentially stripping away the browsers default CSS rules so your site looks as consistent as possible across browsers. 

🔗 - [Read this really in-depth article if you want to learn more](https://medium.com/@riittagirl/a-tale-of-css-resets-and-everything-you-need-to-know-about-them-781849d9b7f2)

Below is a custom CSS reset I’ve been using on my own sites recently, but you’re free to explore other CSS resets out there and use what you feel comfortable with.
```css
/* Custom CSS Reset */
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


## Front-End Resources (Free)
Here are some links to useful resources to learn specific tools to help you improve your front-end development skills.

### CSS Layout Tools
CSS grid/flexbox are two modern layout systems that are a must know for developers these days. The two free courses below helped me get a good grasp on them and they might help you too.

🔗 - [CSS Flexbox Scrimba Course](https://scrimba.com/g/gR8PTE?utm_source=dev.to&utm_medium=referral&utm_campaign=gR8PTE_grid_vs_flexbox)

🔗 - [CSS Grid Scrimba Course](https://scrimba.com/g/gR8PTE?utm_source=dev.to&utm_medium=referral&utm_campaign=gR8PTE_grid_vs_flexbox)
