---
layout: post
title: Controlled VS Uncontrolled Components in React
description: This blogs explains the difference between controlled and uncontrolled components in react
date: 2022-12-09 15:01:35 +0530
image: '/images/controlled-vs-uncontrolled-components-in-react.jpg'
image_caption: 'Photo by [Stephen SIMON](https://twitter.com/codewithsimon)'
tags: [react, react-interview-questions]
---
### Overview

Controlled components are React components that store their state and update their state through props, while uncontrolled components store their state in the DOM. Here's an example of a controlled component:

💡 You can see it live on [Stackblitz](https://react-qffawn.stackblitz.io) and  access the project file are [ here](https://stackblitz.com/edit/react-qffawn?file=src/App.js).

**App.js**

```jsx
import React from 'react';
import './style.css';
import ControlledInput from './controlled.js';
import UncontrolledInput from './uncontrolled.js';

export default function App() {
  return (
    <div>
      <h1>Controlled Vs Un-controlled!</h1>
      <p>Subscribe Channel! </p>
      <ControlledInput />
      <UncontrolledInput />
    </div>
  );
}
```


**controlled.js**

```jsx
import React, { useState } from 'react';

function ControlledInput() {
  const [value, setValue] = useState('');

  function handleChange(event) {
    setValue(event.target.value);
  }

  return (
    <>
      <h3>Controlled Component</h3>
      <input type="text" onChange={handleChange} />
      <h5>{value}</h5>
    </>
  );
}

export default ControlledInput;

```

#### Here's an example of a controlled component:

**uncontrolled.js**

```jsx
import React, { useRef } from 'react';

function UncontrolledInput() {
  const inputRef = useRef(null);

  function handleClick() {
    console.log(inputRef.current.value);
  }

  return (
    <>
      <h3>Un-controlled Component</h3>
      <input type="text" ref={inputRef} />
      <button onClick={handleClick}>Submit</button>
    </>
  );
}

export default UncontrolledInput;

```

![Controlled VS Uncontrolled Component](/images/controlled-vs-uncontrolled-components-in-react-image-1.png)













