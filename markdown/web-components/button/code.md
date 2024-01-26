
# Code

---

# React showcase

Display any other type of code snippet with a **Code** block:

```javascript  
import React, { useEffect, useState } from 'react';
import Clock from 'react-clock';
import 'react-clock/dist/Clock.css';

export default function Component() {
  const [value, setValue] = useState(new Date());

  useEffect(() => {
    const interval = setInterval(() => setValue(new Date()), 1000);

    return () => {
      clearInterval(interval);
    };
  }, []);

  return (
    <div>
      <p>Current time:</p>
      <Clock value={value} />
    </div>
  );
}  
```

```javascript  
import React from 'react';
export default function Button(props) {
 return (
   <button>
     Click me!
   </button>
 );
}  
```

```javascript  
import React from 'react';
import { Button as MuiButton } from '@mui/material';

export default function Button(props) {
 return (
   <MuiButton>
     OK
   </MuiButton>
 );
}  
```

## Storybook stories

Or embed a Storybook story with the **Storybook** block:

  
[Open Storybook Canvas](https://6195b518b76f57003aa69b4c-ynczzfqqyq.chromatic.com/iframe.html?addons=0&stories=0&panel=false&nav=false&id=navigation-navigation--right-click-links&full=1&viewMode=story)  


  
[Open Storybook Canvas](https://6195b518b76f57003aa69b4c-ynczzfqqyq.chromatic.com?addons=1&stories=0&panel=true&nav=false&path=%2Fstory%2Fsurfaces-modals--default)  


```javascript  
class Graph {
  constructor(directed = true) {
    this.directed = directed;
    this.nodes = [];
    this.edges = new Map();
  }

  addNode(key, value = key) {
    this.nodes.push({ key, value });
  }

  addEdge(a, b, weight) {
    this.edges.set(JSON.stringify([a, b]), { a, b, weight });
    if (!this.directed)
      this.edges.set(JSON.stringify([b, a]), { a: b, b: a, weight });
  }

  removeNode(key) {
    this.nodes = this.nodes.filter(n => n.key !== key);
    [...this.edges.values()].forEach(({ a, b }) => {
      if (a === key || b === key) this.edges.delete(JSON.stringify([a, b]));
    });
  }

  removeEdge(a, b) {
    this.edges.delete(JSON.stringify([a, b]));
    if (!this.directed) this.edges.delete(JSON.stringify([b, a]));
  }

  findNode(key) {
    return this.nodes.find(x => x.key === key);
  }

  hasEdge(a, b) {
    return this.edges.has(JSON.stringify([a, b]));
  }

  setEdgeWeight(a, b, weight) {
    this.edges.set(JSON.stringify([a, b]), { a, b, weight });
    if (!this.directed)
      this.edges.set(JSON.stringify([b, a]), { a: b, b: a, weight });
  }

  getEdgeWeight(a, b) {
    return this.edges.get(JSON.stringify([a, b])).weight;
  }

  adjacent(key) {
    return [...this.edges.values()].reduce((acc, { a, b }) => {
      if (a === key) acc.push(b);
      return acc;
    }, []);
  }

  indegree(key) {
    return [...this.edges.values()].reduce((acc, { a, b }) => {
      if (b === key) acc++;
      return acc;
    }, 0);
  }

  outdegree(key) {
    return [...this.edges.values()].reduce((acc, { a, b }) => {
      if (a === key) acc++;
      return acc;
    }, 0);
  }
}  
```