# REACT CRASH COURSE

### STARTUP

`npx create-react-app my-app`

everything outputs thru `index.html`

1. get rid of `index.css` and dependencies, replace 

inside of `App.css` with

```react
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}

a {
  color: #333;
  text-decoration: none;
}
```

2. get rid of `logo.svg` and dependencies
3. SAVE!



### CLEANUP

1. create `components` create `Todos.js`

2. copy stuff from `App.js` and change 

   `class`, `export`

3. delete the import App.css

4. go to App.js and `import` Todos.js

   `import './components/Todos'`

   *NOTE: `.` suggests that it is from same directory*

### STATES

1. you need states that MULTIPLE components can access

2. All To-do's go in **main app**

3. `App.js`

   create a `state`

   ```react
       todos: [
         {
           id:1,
           title: 'Take out the trash',
           completed: false
         },
         {
           id:2,
           title: 'Dinner with wife',
           completed: false
         },
         {
           id:3,
           title: 'Meeting with boss',
           completed: false
         },
       ]
   ```

   ...an *array of **objects***

4. put it in the render  section

   `console.log(this.state.todos)`

   you can see it in **console log** of browser, array has been created.

5. save this thing as a **prop**, get rid of step **4** and change in `App.js`

   `<Todos todos={this.state.todos}/>`

   see this in React Developer Tools > Todos 

6. `rce` and then **TAB** allows me to create **component files**  very quickly

7. Create a new `TodoItem.js` file under `components` and use step 6 to occupy it. Fill in the `div` with `<p> Hello </p>` or something

### Adding Features / List, Background, Buttons

1. Everything is passed down as props, and the files go down-level. 

### Filter Method

1. 