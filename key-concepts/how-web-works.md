### TCP Handshake

1. Client sends a SYN (synchronize) request to the server.
2. Server replies with a SYN-ACK (synchronize-acknowledge).
3. Client replies with an ACK (acknowledge).

### SSL (Secure Sockets Layer) Handshake

1. Client sends a message to the server which includes:
   - SSL/TLS version
   - Cryptographic algorithms supported by the client
   - Data compression methods supported by the client
2. Server responds with a message that contains:
   - Cryptographic algorithm chosen by the server
   - Session ID
   - Digital certificate
   - Server's public key
3. Client validates the server certificate.
4. Client sends a pre-master secret, encrypted with the server's public key.
5. Client sends a "finished" message encrypted with the session key.
6. Server sends a "finished" message encrypted with the session key.
7. Secure communication begins.

*At any time, the browser can make 6-8 requests in parallel; the rest of the requests are queued.*

*CSS is render-blocking - until CSS is loaded, nothing will be rendered.*

*JavaScript is parser-blocking - until JavaScript is loaded, execution won't proceed to the next line.*

### When an API Call is Made

1. Request goes to ISP, which queries DNS and returns the IP address to the client.
2. Client and server (IP) perform a TCP handshake.
3. Client and server (IP) perform an SSL handshake.
4. Client makes a request to the server.

### How HTML is Rendered

1. HTML file is loaded, and all required assets (CSS, JS, images, etc.) are loaded.
2. HTML DOM is built.
3. CSSOM is built.
4. JavaScript is executed.
5. DOM and CSSOM are merged into the render tree.
6. Layout - Determines the number of boxes, their placement, size, etc., and draws the skeleton.
7. Paint - CSS is applied.
8. Compositing - Based on layers/z-index, whatever comes to the top is visible.
