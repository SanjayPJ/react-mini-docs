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
