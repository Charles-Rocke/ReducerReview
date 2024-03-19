# Learnings

**reducers:**

- used when state is more complex, instead of one piece of state, state is usually an object

**useReducer() hook:**

- is a more advanced and more complex way of managing state instead of the useState hook.
- works with a reducer function (a pure function that always takes in a previous state and an action as an argument and then returns the next state)
- 'useReducer()' takes in the initial state and the reducer function ( useReducer(reducer, initialState) )
- 'useReducer()' first argument must be a reducer function and the second arg must be the state
- 'useReducer()' returns current state and dispatch function that is used to update state
- 'dispatch()' sends an action to the reducer that is essentially an action identifier (keyword for a specific action) for ex. if the action = "login", then the login action in the reducer will be called and performed
- 'dispatch()' receives an object that defines the type of action and the payload that is passed in
  ( dispatch({ type: "dec", payload: -1 }) ), the entire object ( { type: "dec", payload: -1 } ) is considered the action
- payloads aren't always necessary (if the action can be hardcoded in/ doesn't need to accept dynamic payloads)
  for ex. { type: "dec", payload: -1 } --> { type: "dec"}
  and in the reducer function:
  'function reducer() { if (action.type === "dec") return state - action.payload; }' -->
  { if (action.type === "dec") return state - 1; }

**function reducer():** takes in the current state and an action ( reducer(currentState, action) )

- the idea of the reducer function ( 'function reducer(currentState, action)' ) is to take the current state + the action and the result (=), will be the next state
- when returning new state, you want to keep the same shape. So if the state is an object you will spread the object and add the value that will be overridden and changed.
  for ex. if the state contained a count and a step {count: 0, step: 1} and we wanted to change the count, this is how we would do it:
  return { ...state, count: state.count + 1 }
  this will keep everything else the same in the object and change/override the count state

# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
