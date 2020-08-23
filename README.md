# Frontend-Starter-Kit (WIP) 🚀 
Here are some quick start tips/resources I personally wish I had been aware of when I first started my journey into the world of front-end development. I am assuming you already know the basics and made a simple project or two. If you are an absolute beginner I go more in depth of how to get started from zero in my blog post here.


## CSS Resets

Browsers like Chrome, Firefox, Internet Explorer etc. can have different default CSS rules for certain elements. Due to this if you are not careful you can have things look good on one browser but weird on another. 

CSS resets help solve this problem by essentially stripping away the browsers default CSS rules so your site looks as consistent as possible across browsers. 

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
## Making Api Request

### XMLHttpRequest (Supports Older Browsers)

#### Get Request Example
```js
const xhr = new XMLHttpRequest();
// Make a get request to retrieve some fake JSON for testing
xhr.open('GET', 'https://jsonplaceholder.typicode.com/posts');

// If you want to send/receive credentials like cookies
xhr.withCredentials = true;
xhr.send();
xhr.onload = () => {
  console.log(xhr);
  if(xhr.status === 200){
    console.log(JSON.parse(xhr.response));
  }  else  {
    console.log('It didn\'t work D:', xhr.status, xhr.statusText)
  }
}
```

#### Post Request Example

```js 
const xhr = new XMLHttpRequest;
xhr.open('POST', 'https://example.com/login');
xhr.withCredentials = true;
xhr.setRequestHeader("Content-Type", "application/json;charset=UTF-8");
xhr.send(JSON.stringify({username: "Sam123", password: "secretpa$$word123"}));
xhr.onload = () => console.log(xhr.response);
```

[MDN - XMLHttpRequest](https://developer.mozilla.org/en-US/docs/Web/API/XMLHttpRequest)

[Javscript.info - XMLHttpRequest](https://javascript.info/xmlhttprequest)

### Fetch

#### Get Request Example

```js
fetch('https://jsonplaceholder.typicode.com/posts')
.then(response => {
  return response.json();
})
.then(data => {
  console.log(data);
})
```
#### Post Request Example
```js
fetch('https://example.com/login', {
  method: 'POST',
  credentials: 'include',
  headers: {
    'Content-Type': 'application/json;charset=UTF-8',
  },
  body: JSON.stringify({username: "Sam123", password: "secretpa$$word123"});
})
.then(response => {
  return response.json();
})
.then(data => {
  console.log(data);
})
```
[MDN - Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

[Javascript.info - Fetch](https://javascript.info/fetch)

#### Sending Form Data
```html
<form onsubmit="return login(event)">
  <label>
    Username:
    <input type="text" name="username">
  </label>
  <label> 
    Password: 
    <input type="text" name="password">
  </label>
</form>

<script>
  const login = async (e) => {
    e.preventDefault();
    const loginForm = document.querySelector('form');
    const formData = new FormData(loginForm);
    const response = await fetch('https://example.com/login', { method: 'POST', credentials: 'include', body: formData });
    const data = await response.json();
    console.log(data);
    return false;
  }
</script>
```
[MDN - FormData](https://developer.mozilla.org/en-US/docs/Web/API/FormData)

[Javascript.info - FormData](https://javascript.info/formdata)

### CSS Grid/Flexbox
CSS grid/flexbox are two modern layout systems that are a must know for developers these days. The two free courses below helped me get a good grasp on them and they might help you too.

🔗 - [CSS Flexbox Scrimba Course](https://scrimba.com/g/gR8PTE?utm_source=dev.to&utm_medium=referral&utm_campaign=gR8PTE_grid_vs_flexbox)

🔗 - [CSS Grid Scrimba Course](https://scrimba.com/g/gR8PTE?utm_source=dev.to&utm_medium=referral&utm_campaign=gR8PTE_grid_vs_flexbox)
