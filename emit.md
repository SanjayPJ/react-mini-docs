## Emiting Events

- *Create a function inside parent component*
- *Pass function as a prop*

```
onClick={this.props.deleteClickHandler}
```

- *call fuction from child component*
- *Inside parent component bind variables*

```
deleteClickHandler={this.deleteClickHandler.bind(this, contact.id)}
```

