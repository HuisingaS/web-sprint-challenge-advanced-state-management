1. What problem does the context API help solve?

    Simplifies the handling of state - no need for handing down props

2. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

    Actions: are payloads of information that send data from your application to your store. They are the only source of information for the store. You send them to the store using store.dispatch(). Actions are plain JavaScript objects. Actions must have a type property that indicates the type of action being performed. Types should typically be defined as string constants. Once your app is large enough, you may want to move them into a separate module.

    Reducers: specify how the application's state changes in response to actions sent to the store. Remember that actions only describe what happened, but don't describe how the application's state changes.

    Store: holds the whole state tree of your application. The only way to change the state inside it is to dispatch an action on it. A store is not a class. It's just an object with a few methods on it. To create it, pass your root reducing function to createStore.

3. What is the difference between Application state and Component state? When would be a good time to use one over the other?

    Application state is global, where as, component state is local. Flux or a flux-like library like Redux, use what they call "stores" to hold application state. That means any component, anywhere in the app can access it (kind of like a database) so long as they hook into it. Component state however, lives within that specific component. As such, it can only be updated within that component and passed down to its children via props.

4. Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

    Redux Thunk: A middleware that lets you call action creators that return a function instead of an action object. That function receives the store's dispatch method, which is then used to dispatch regular synchronous actions inside the body of the function once the asynchronous operations have completed.

5. What is your favorite state management system you've learned and this sprint? Please explain why!

    Async Redux - State is easier to handle, and the need for props is not crucial.