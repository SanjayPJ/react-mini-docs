## React Router

*Install*

```
npm install --save react-router-dom
```

*Inside App.js*

```
import { BrowserRouter as Router, Route, Switch } from "react-router-dom";
```

*jsx*

```
<ContactContextProvider>
    <Router>
        <Navbar title="Contact Manager"/>
        <Switch>
            <Route exact path="/" component={Contents} />
            <Route exact path="/contact/add" component={AddContact} />
        </Switch>
    </Router>
</ContactContextProvider>
```
