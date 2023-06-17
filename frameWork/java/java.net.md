[[Java]] clients, servers, sockets
[`docs`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/package-summary.html)

# Sockets
>Sockets are means to establish a communication link between machines over the network. The java.net package provides 4 kinds of Sockets:

- [`Socket`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/Socket.html "class in java.net") is a TCP client API, and will typically be used to [connect](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/Socket.html#connect(java.net.SocketAddress)) to a remote host.
- [`ServerSocket`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/ServerSocket.html "class in java.net") is a TCP server API, and will typically [accept](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/ServerSocket.html#accept()) connections from client sockets.
- [`DatagramSocket`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/DatagramSocket.html "class in java.net") is a UDP endpoint API and is used to [send](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/DatagramSocket.html#send(java.net.DatagramPacket)) and [receive](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/DatagramSocket.html#receive(java.net.DatagramPacket)) [datagram packets](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/DatagramPacket.html "class in java.net").
- [`MulticastSocket`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/MulticastSocket.html "class in java.net") is a subclass of `DatagramSocket` used when dealing with multicast groups.

Sending and receiving with TCP sockets is done through InputStreams and OutputStreams which can be obtained via the [`Socket.getInputStream()`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/Socket.html#getInputStream()) and [`Socket.getOutputStream()`](https://docs.oracle.com/en/java/javase/20/docs/api/java.base/java/net/Socket.html#getOutputStream()) methods.

```java
Socket socket = new Socket();
socket.connect(new java.net.InetSocketAddress(host, port), 1000);
socket.close();
```
