---
layout: post
title: What are Pure Components in React?
description: Understand what are pure components in react and its usecases.
date: 2023-02-21 10:01:35 +0300
image: '/images/what-are-pure-components-in-react.jpg'
image_caption: 'Photo by [Stephen SIMON](https://twitter.com/codewithsimon)'
tags: [react]
---

In React, components are the building blocks of your application's user interface. They are responsible for rendering content to the screen, handling user events, and managing state.

A pure component is a special type of component that only re-renders when its props or state change. If the props and state remain the same, the pure component will not re-render, which can help to optimize performance and reduce unnecessary updates.

To create a pure component in React, you can extend the **`React.PureComponent`** class instead of the regular **`React.Component`** class. Here's an example:

```jsx
class MyComponent extends React.PureComponent {
  render() {
    return (
      <div>
        <p>Name: {this.props.name}</p>
        <p>Age: {this.props.age}</p>
      </div>
    );
  }
}
```

In this example, **`MyComponent`** is a pure component that takes two props, name and age, and renders them to the screen. Because it extends **`React.PureComponent`**, it will only re-render if its props or state change.

By using pure components in your application, you can help to optimize performance and reduce unnecessary updates. However, it's important to keep in mind that pure components are not always appropriate for every use case. If you have complex logic or data dependencies, you may need to use a regular React.Component instead.