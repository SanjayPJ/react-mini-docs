## Working with Forms

#### Controled Components

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

#### Uncontrolled Components

- *Add a defailt value*
- *Add ref attribute*

```
<input defaultValue={phone} name="phone" type="text" className="form-control" ref={this.phoneInput} />
```
- *Add constructor*

```
constructor(props) {
    super(props);

    this.nameInput = React.createRef();
    this.emailInput = React.createRef();
    this.phoneInput = React.createRef();
}
```

- *On Submit*

```
onSubmitHandler = (e) => {
    e.preventDefault();

    const contact = {
        name: this.nameInput.current.value,
        email: this.emailInput.current.value,
        phone: this.phoneInput.current.value,
    }

    console.log(contact);
}
```
