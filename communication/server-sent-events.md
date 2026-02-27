## Server Side Events (SSE)

Server-Sent Events (SSE) is a technology that allows a server to push real-time updates to a web client over a single, long-lived HTTP connection. It is a simple and efficient way to enable real-time communication between a server and a web browser without the need for complex protocols like WebSockets.

### Workflow of SSE

1. **Client Request**: The client (usually a web browser) initiates a connection to the server by sending an HTTP request to a specific endpoint that is designed to handle SSE.

2. **Server Response**: The server responds with a special content type (`text/event-stream`) and keeps the connection open. The server can then send data to the client in a specific format.

3. **Data Format**: The server sends data in a simple format where each message is prefixed with `data:` and ends with a double newline (`\n\n`). For example:

   ```
   data: Hello, this is a message from the server!\n\n
   ```

4. **Client Handling**: The client listens for incoming messages from the server and processes them as they arrive. This allows for real-time updates without the need for the client to continuously poll the server.

### Benefits of SSE

- **Simplicity**: SSE is easier to implement than WebSockets for many use cases, especially when the communication is primarily one-way (server to client).

- **Built-in Reconnection**: SSE has built-in support for automatic reconnection if the connection is lost, which simplifies error handling on the client side.

- **HTTP/2 Support**: SSE can take advantage of HTTP/2 features, such as multiplexing, which can improve performance and reduce latency.

### Limitations of SSE

- **One-Way Communication**: SSE is designed for server-to-client communication and does not support client-to-server messages. If bidirectional communication is needed, WebSockets may be a better choice.

- **Browser Support**: While most modern browsers support SSE, it may not be available in older browsers or certain environments, which can limit its use in some applications.

- **Scalability**: Since SSE relies on long-lived HTTP connections, it may not scale well for applications with a large number of concurrent users, as each user requires a separate connection to the server. Also, each browser can make 6-8 connections in parallel, and this will reduce the no. of api calls that can be made to the server.

### Use Cases for SSE

- **Live Updates**: SSE is ideal for applications that require real-time updates, such as news feeds, stock tickers, or social media notifications.

- **Chat Applications**: While WebSockets are often used for chat applications, SSE can be sufficient for scenarios where the communication is primarily from the server to the client.

- **Monitoring Dashboards**: SSE can be used to push real-time data to monitoring dashboards, allowing users to see live metrics and updates without refreshing the page.
