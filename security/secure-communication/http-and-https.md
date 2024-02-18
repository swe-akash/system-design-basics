# HTTP and HTTPS

HTTP (Hypertext Transfer Protocol) and HTTPS (Hypertext Transfer Protocol Secure) are both protocols used for transferring data over the web. They define how messages are formatted and transmitted, and how web servers and browsers should respond to various commands.

1. [HTTP](#http)
2. [HTTPS](#https)

## HTTP

- It is a very light weight protocol.
- It operates at the application layer (Layer 7) of the OSI model.
- It is a stateless protocol, meaning each command is executed independently without any knowledge of the previous commands.
- Data is sent over the network as plain text, making it unsecure.
- Listens on port 80 by default.

### HTTP/1.0

- The first version of HTTP, introduced in 1996.
- Simple and straightforward, but inefficient for modern web applications due to its limitation of one request per connection.

### HTTP/1.1

- Introduced in 1997 as an improvement over HTTP/1.0.
- Allowed multiple requests to be sent over a single TCP connection, reducing latency and improving performance. However, responses must be received in the same order as requests.
- Widely used but has limitations in handling concurrent requests and suffers from head-of-line blocking, where subsequent requests on the same connection must wait for previous requests to complete. If one request is blocked, subsequent requests are affected.

### HTTP/2

- Introduced in 2015 by the HTTP Working Group as an effort to improve web performance.
- Major improvements over HTTP/1.1, including multiplexing, header compression, and server push.
- Allows multiple streams of requests to be sent to the same server over a single TCP connection. Each stream is independent and does not need to be sent/received in order.
  
### HTTP/3

- The latest version of HTTP, still under development at the time of writing (2024).
- Aims to further enhance performance and security, particularly for mobile and low-latency applications.
- Utilizes QUIC (Quick UDP Internet Connections) as its underlying transport protocol, which is designed to reduce latency and improve reliability compared to TCP.

## HTTPS

- HTTPS is heavier than HTTP.
- HTTPS operates at the transport layer (Layer 4) of the OSI model.
- Data is encrypted before transmission, ensuring security.
- Listens on port 443 by default.

### How HTTPS works?

1. Client initiates a connection request to the server.
2. Server responds with the certificate and public key.
3. Client verifies the certificate, then generates a session key and sends it to the server after encrypting it with the public key.
4. Server decrypts the session key using its private key.
5. Both client and server use the session key to encrypt and decrypt transferred data.
6. The session key is valid for that particular session only.
