## Passing Props

```
<Navbar title="sample title"/>
```

- Inside class based components

```
{this.props.title}
```

- Inside function based components

```
{props.title}
```

### Default Props

```
Componentname.defaultProps = {
    title: "Helllo"
}

```

### PropTypes

```
Componentname.propTypes = {
    title: PropTypes.object.isRequired
}
```
