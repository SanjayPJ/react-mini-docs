## Working with Forms

- *Add variables to state*

- *Link that variables to inputs*

```
<input onChange={this.onChangeHandler} name="name" type="text" className="form-control" />
```

- *Add method to handle event*

```
  onChangeHandler = (e) => {
      this.setState({
          [e.target.name]: e.target.value
      });
  }
```
