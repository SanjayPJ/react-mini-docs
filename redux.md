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

## TypeError: Object(…) is not a function (redux)

```
npm update
```
------


- *create `src/actions/types.js`*

```
export const GET_CONTACTS = 'GET_CONTACTS'
```

- *create `src/actions/contactActions.js`*


```
import { GET_CONTACTS } from "./types";

export const getContacts = () => {
    return {
        type: GET_CONTACTS
    }
}
```

- *Inside a child component for accessing redux state data*

```
import { connect } from  'react-redux'
import { getContacts } from '../../actions/contactActions'
```

```
const mapStateToProps = state => ({
  contacts: state.contact.contacts
});

export default connect(mapStateToProps, { getContacts })(Contacts);
```

- *can access it through props*

- *if additional parameters are present ->*

```
export const deleteContact = (id) => {
    return {
        type: DELETE_CONTACT,
        payload: id
    }
}

export const addContact = (contact) => {
    return {
        type: ADD_CONTACT,
        payload: contact
    }
}
```

### Async

```
export const getContacts = () => async dispatch => {
    const res = await Axios.get('https://jsonplaceholder.typicode.com/users')
    dispatch({
        type: GET_CONTACTS,
        payload: res.data
    })
}

export const getContact = (id) => async dispatch => {
    const res = await Axios.get('https://jsonplaceholder.typicode.com/users/' + id)
    dispatch({
        type: GET_CONTACT,
        payload: res.data
    })
}

export const deleteContact = (id) => async dispatch => {
    await Axios.delete(`https://jsonplaceholder.typicode.com/users/${id}`);
    dispatch({
        type: DELETE_CONTACT,
        payload: id
    })
}

export const addContact = (contact) => async dispatch => {
    const res = await Axios.post('https://jsonplaceholder.typicode.com/users', contact);
    dispatch({
        type: ADD_CONTACT,
        payload: res.data
    })
}


export const updateContact = (contact) => async dispatch => {
    const res = await Axios.put('https://jsonplaceholder.typicode.com/users/' + contact.id, contact);
    dispatch({
        type: UPDATE_CONTACT,
        payload: res.data
    })
}
```
