## React Redux

```
npm i redux react-redux redux-thunk
```

- *Create store.js inside src folder*

```
import { createStore, applyMiddleware, compose } from 'redux';
import thunk from 'redux-thunk';
import rootReducer from './reducers';

const initialState = {};

const middleware = [thunk];

const store = createStore(
    rootReducer,
    initialState,
    compose(
        applyMiddleware(...middleware),
        window.__REDUX_DEVTOOLS_EXTENSION__ && window.__REDUX_DEVTOOLS_EXTENSION__()
    )
);

export default store;

```

- *Inside App.js*

```
import { Provider } from 'react-redux';
import store from './store';
```
- *then wrap everything inside `<Provider store={store}></Provider>`*
- *Create reducers folder inside src folder*
- *Create index.js inside reducers folder*
- *Inside index.js*

```
import { combineReducers } from 'redux';
import contactReducer from './contactReducer';

export default combineReducers({
  contact: contactReducer
});
```

- *Inside contactReducer*

```
const initialState = {};

export default function(state = initialState, action) {
  switch (action.type) {
    default:
      return state;
  }
}

```

##TypeError: Object(…) is not a function (redux)

```
npm update
```
