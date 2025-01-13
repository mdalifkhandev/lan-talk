# MERN Stack Project: Build and Deploy a Real Time Chat App | JWT, Socket.io

![Demo App](https://i.ibb.co/fXmZdnz/Screenshot-10.png)

[Video Tutorial on Youtube](https://youtu.be/HwCqsOis894)

Some Features:

-   🌟 Tech stack: MERN + Socket.io + TailwindCSS + Daisy UI
-   🎃 Authentication && Authorization with JWT
-   👾 Real-time messaging with Socket.io
-   🚀 Online user status (Socket.io and React Context)
-   👌 Global state management with Zustand
-   🐞 Error handling both on the server and on the client
-   ⭐ At the end Deployment like a pro for FREE!
-   ⏳ And much more!

### Setup .env file

```js
PORT=...
MONGO_DB_URI=...
JWT_SECRET=...
NODE_ENV=...
```

### Build the app

```shell
npm run build
```

### Start the app

```shell
npm start
```

### Real-time Updates with Socket.io

To enable real-time updates, ensure that your server is set up to handle Socket.io connections and that the client is correctly configured to connect to the server.

1. Install Socket.io on both server and client:
    ```shell
    npm install socket.io
    npm install socket.io-client
    ```

2. Set up the server to handle Socket.io connections:
    ```js
    const io = require('socket.io')(server, {
        cors: {
            origin: "http://localhost:3000",
            methods: ["GET", "POST"]
        }
    });

    io.on('connection', (socket) => {
        console.log('a user connected');
        
        socket.on('disconnect', () => {
            console.log('user disconnected');
        });
    });
    ```

3. Connect the client to the server:
    ```js
    import io from 'socket.io-client';
    const socket = io("http://localhost:5000");
    ```

# [Video Tutorial](https://www.youtube.com/watch?v=HwCqsOis894&list=PLNEhktk_WNzpC3JnwmksayfVEK3qhFc6S&ab_channel=AsaProgrammer)