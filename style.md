## Styling Components

```
const divStyle = {
  color: 'blue',
  backgroundImage: 'url(' + imgUrl + ')',
};

function HelloWorldComponent() {
  return <div style={divStyle}>Hello World!</div>;
}
```

```
<div style={{ height: '10%' }}>
  Hello World!
</div>
```

*Otherwise add include it into component js file*


### Include Bootstrap

```
npm install bootstrap
```

- In index.js

```
import 'bootstrap/dist/css/bootstrap.min.css'
```
