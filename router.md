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

### Links

```
import { Link } from "react-router-dom";
```

```
<Link className="nav-link" to="/">Home <span className="sr-only">(current)</span></Link>
```

### Params

```
<Route exact path="/contact/:id" component={Contact} />
```

*Can access it through*

```
this.props.match.params.id
```

### Redirect

```
this.props.history.push('/');
```

### 404

```
<Router>
    <Switch>
        <Route exact path="/" component={Contents} />
        <Route exact path="/about/:id" component={About} />
        <Route exact path="/contact/add" component={AddContact} />
        <Route component={NotFound} />
    </Switch>
</Router>
```
