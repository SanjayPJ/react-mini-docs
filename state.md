## State

```
import React from 'react';
import Navbar from './components/Navbar'
import Contact from './components/Contact'
import './App.css'

export default class App extends React.Component {

    constructor() {
        super();
        this.state = {
            contacts: [{
                    "id": 1,
                    "name": "Leanne Graham",
                    "username": "Bret",
                    "email": "Sincere@april.biz",
                    "address": {
                        "street": "Kulas Light",
                        "suite": "Apt. 556",
                        "city": "Gwenborough",
                        "zipcode": "92998-3874",
                        "geo": {
                            "lat": "-37.3159",
                            "lng": "81.1496"
                        }
                    },
                    "phone": "1-770-736-8031 x56442",
                    "website": "hildegard.org",
                    "company": {
                        "name": "Romaguera-Crona",
                        "catchPhrase": "Multi-layered client-server neural-net",
                        "bs": "harness real-time e-markets"
                    }
                },
                {
                    "id": 2,
                    "name": "Ervin Howell",
                    "username": "Antonette",
                    "email": "Shanna@melissa.tv",
                    "address": {
                        "street": "Victor Plains",
                        "suite": "Suite 879",
                        "city": "Wisokyburgh",
                        "zipcode": "90566-7771",
                        "geo": {
                            "lat": "-43.9509",
                            "lng": "-34.4618"
                        }
                    },
                    "phone": "010-692-6593 x09125",
                    "website": "anastasia.net",
                    "company": {
                        "name": "Deckow-Crist",
                        "catchPhrase": "Proactive didactic contingency",
                        "bs": "synergize scalable supply-chains"
                    }
                }
            ]
        }
    }
    render() {
        const { contacts } = this.state
        return (
            <div>
          <Navbar title="Contact Manager"/>
          <div className="container">
          {contacts.map(contact => (
            <Contact key={contact.id} name={contact.name} email={contact.email} phone={contact.phone}/>
            ))}
          </div>
        </div>
        );
    }
}
```

### OR

```
import React from 'react';
import Navbar from './components/Navbar'
import Contact from './components/Contact'
import './App.css'

export default class App extends React.Component {

    state = {
        contacts: [{
                "id": 1,
                "name": "Leanne Graham",
                "username": "Bret",
                "email": "Sincere@april.biz",
                "address": {
                    "street": "Kulas Light",
                    "suite": "Apt. 556",
                    "city": "Gwenborough",
                    "zipcode": "92998-3874",
                    "geo": {
                        "lat": "-37.3159",
                        "lng": "81.1496"
                    }
                },
                "phone": "1-770-736-8031 x56442",
                "website": "hildegard.org",
                "company": {
                    "name": "Romaguera-Crona",
                    "catchPhrase": "Multi-layered client-server neural-net",
                    "bs": "harness real-time e-markets"
                }
            },
            {
                "id": 2,
                "name": "Ervin Howell",
                "username": "Antonette",
                "email": "Shanna@melissa.tv",
                "address": {
                    "street": "Victor Plains",
                    "suite": "Suite 879",
                    "city": "Wisokyburgh",
                    "zipcode": "90566-7771",
                    "geo": {
                        "lat": "-43.9509",
                        "lng": "-34.4618"
                    }
                },
                "phone": "010-692-6593 x09125",
                "website": "anastasia.net",
                "company": {
                    "name": "Deckow-Crist",
                    "catchPhrase": "Proactive didactic contingency",
                    "bs": "synergize scalable supply-chains"
                }
            },
        ]
    }
    render() {
        const { contacts } = this.state
        return (
            <div>
          <Navbar title="Contact Manager"/>
          <div className="container">
          {contacts.map(contact => (
            <Contact key={contact.id} name={contact.name} email={contact.email} phone={contact.phone}/>
            ))}
          </div>
        </div>
        );
    }
}
```

### Modify State from a Component

```
this.setState({ show_info: !this.state.show_info })
```
