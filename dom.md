## Render Data to DOM

### Show data variables

```
function App() {
    const name = "Sanjay PJ"
    return (
        <div className="App">
          <h1>Hello {name}!</h1>
        </div>
    );
}
```

### If Condition

```
function App() {
    const show_data = true
    return (
        <div className="App">
          {show_data ? <h1>Sanjay PJ</h1> : null}
        </div>
    );
}
```
### Loop Through

```
return (
    <div>
  {contacts.map(contact => (
    <Contact key={contact.id} name={contact.name} email={contact.email} phone={contact.phone}/>
    ))}
</div>
);
```
