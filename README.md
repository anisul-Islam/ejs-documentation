# My Embedded Javascript (ejs) Documentation

### Total Chapters are following

1.  Introduction ejs
2.  Passing data
3.  if else
4.  loop
5.  layout
6.  styling
7.  deploy on heroku

<br />

### [1. Introduction to ejs](https://youtu.be/x9o3fxS_xdM)

#### What is ejs & Why ejs?

- ejs stands for embedded javascript
- ejs is a templating language.
- templating language helps us to manipulate dynamic content in HTML document.
- Templating language: ejs, handlebars, pug etc.
- Ejs allows us to run plain js in HTML
- Ejs simple, light weight, fast
- Most downloaded templating language on npm
- Founded in Feb, 2011
- how to use ejs

  ```js
    // first install ejs:
    npm install ejs

    // inside the server
    app.set('view engine', 'ejs’);

    // create index.ejs inside views folder
    res.render('index',{});

  ```

### [2. Passing data to ejs]()

- create and pass the data
- syntax: `<%= variable %>`

  ```js
  let pLanguages = ["c", "c++"];

  app.get("/", (req, res) => {
    res.render("index", { plNames: pLanguages });
  });

  //inside the index.ejs
   <li><%= plNames[0] %></li>
  ```

### [3. if else in ejs]()

- if, else syntax:

  ```js
    <% if () { %>
        // do whatever
     <% } else { %>
        // do whatever
     <% } %>
  ```

  ```js
  <% if(plNames){ %>
  <li><%= plNames[x] %></li>
  <% }else{ %>
  <p>no data found</p>
  <% } %>
  ```

### [4. loop in ejs]()

- loop control statement
- syntax:

  ```js
    <% for () { %>
        // do whatever
     <% } %>
  ```

  ```js
  <% for(let x=0; x<plNames.length; x++){ %>
    <li><%= plNames[x] %></li>
    <% } %></plNames.length;
  >
  ```

### [5. layout in ejs]()

- create layout and use it anywhere
- To use a layout syntax : <%- include("layout/header") %>

### [6. styling in ejs]()

### [7. deploy on heroku]()

- project link on github: https://github.com/anisul-Islam/ejs-youtube-project
