---
layout: post
title: Building a Real-Time Chat App with React and Socket.io
description: Walk through the process of creating a chat app from scratch using React and Socket.io
date: 2023-02-22 10:01:35 +0300
image: '/images/building-a-real-time-chat-app-with-react-and-socket-io.jpg'
image_caption: 'Photo by [Stephen SIMON](https://twitter.com/codewithsimon)'
tags: [react]
---


Socket.io is a JavaScript library that allows you to create real-time, bidirectional, and event-based communication between the client and server. It uses WebSockets, which provides low latency, full-duplex communication over a single TCP connection.

Socket.io is a great choice for building real-time chat applications, as it makes it easy to send and receive messages between clients in real-time.

### ⭐ Setting up a new React app
To get started, we'll create a new React app using create-react-app. Open up your terminal and type the following command:

```
npx create-react-app chat-app
```

This will create a new React app in a directory called chat-app. Change into the directory by typing:

```
cd chat-app
```

Now, let's start the development server by typing:

```
npm start
```

This will start the development server at http://localhost:3000. You should see the default React app running in your browser.

### 📩 Installing Socket.io

Now that we have a React app set up, let's install Socket.io. In your terminal, type the following command:

```
npm install socket.io-client
```

This will install the Socket.io client library, which we'll use to communicate with the server.

### 🏨 Setting up the server

Next, we'll set up a simple Node.js server that uses Socket.io. Create a new file in the root directory of your project called **server.js**. In this file, we'll write some code to set up a new Socket.io server.

```jsx
const express = require('express');
const app = express();
const http = require('http').Server(app);
const io = require('socket.io')(http);

io.on('connection', (socket) => {
  console.log('A user connected');
});

http.listen(4000, () => {
  console.log('Server listening on port 4000');
});
```
This code sets up an Express app, creates a new HTTP server, and then creates a new Socket.io server that listens for connections on the HTTP server.

When a client connects to the server, Socket.io will emit a connection event. In our code, we're logging a message to the console when this event is emitted.

Finally, we're starting the server and listening on port 4000.

### 🤙 Connecting to the server from React

Now that we have a server set up, let's connect to it from our React app. Open up App.js in your src directory and add the following code:

```jsx
import { io } from 'socket.io-client';
const socket = io('http://localhost:4000');

function App() {
  return (
    <div className="App">
      <h1>Welcome to the Chat App</h1>
    </div>
  );
}

export default App;
```
Here, we're importing the Socket.io client library and creating a new Socket.io instance that connects to our server at http://localhost:4000.

### ☎ Sending and receiving messages
Now that we have a connection to the server, let's send and receive messages between clients.

Add the following code to App.js:

```jsx
import { useState, useEffect } from 'react';

function App() {
  const [messages, setMessages] = useState([]);
  const [inputValue, setInputValue] = useState('');

  useEffect(() => {
    socket.on('message', (message) => {
      setMessages((messages) => [...messages, message
```

