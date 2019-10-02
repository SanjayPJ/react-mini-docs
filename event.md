## Event Handling

*Bind a method to element*

```
<a className="text-primary" onClick={this.hideSomething.bind(this)}>
```

*Add method before render method*

```
export default class Contact extends React.Component {
    state = {}
    hideSomething = () => {
        console.log(this.state);
    }

    render() {
        const { name, email, phone } = this.props
        return (
            <div>
            	<div className="card mt-3">
            	  <div className="card-header">
            	    <h4>{name} <a className="text-primary" onClick={this.hideSomething.bind(this)}>*</a></h4>
            	  </div>
            	  <ul className="list-group list-group-flush">
            	    <li className="list-group-item">{email}</li>
            	    <li className="list-group-item">{phone}</li>
            	  </ul>
            	</div>
            </div>
        );
    }
}
```
