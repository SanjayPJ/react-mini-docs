## Components

### Creating components

- *Inside src folder create components folder*

- *Create `ComponentName.js` file* 

```
import React from 'react';

export default class Todos extends React.Component {
    state = {
        someVar: "this is amazing!!!!"
    }

    render() {
        return (
            <div>
            	<h1>Todos</h1>
            </div>
        );
    }
}
```
- *Import into parent component*

### Class Based Component

```
import React from 'react';

export default class ComponentName extends React.Component {
	render() {
		return (
			<div></div>
		);
	}
}
```

### Function Based Components

```
import React from 'react';

const ComponentName = (props) => {
  return (
    <div></div>
  )
}

export default ComponentName;
```
