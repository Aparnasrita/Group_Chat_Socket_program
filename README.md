# Group Chat Socket Programming

## Introduction

Socket programming is a method of communication between two computers using a network protocol, typically TCP/IP. In this project, we utilize socket programming in C++ to implement a real-time group chat system. The system comprises a server and multiple clients. The server manages incoming client connections and broadcasts messages to all connected clients, while clients can send and receive messages.

## What is Socket Programming?

Socket programming allows for the sending and receiving of messages over a network. It provides mechanisms to create a socket on the client or server side, connect sockets, and listen for data on sockets. In essence, it's the backbone of most internet communication today, from web browsing to chat applications.

### Key Concepts:

- **Socket**: An endpoint for sending or receiving data. It binds to a specific port on a machine.
- **Port**: A logical point for receiving and sending data. Each service on a machine is associated with a unique port number.
- **IP Address**: A unique string of numbers separated by periods that identifies each computer using the Internet Protocol to communicate over a network.

## Implementation

### Server

The server is responsible for:

1. Creating a socket and binding it to a specific port.
2. Listening for incoming client connections.
3. Accepting client connections and handling them using multi-threading.
4. Broadcasting messages received from one client to all other connected clients.

### Client

The client's responsibilities are:

1. Creating a socket.
2. Connecting to the server using the server's IP address and port number.
3. Sending and receiving messages.

## Features

- **Multi-threading**: Utilizes multi-threading to handle multiple clients simultaneously, ensuring real-time communication.
- **Real-time Communication**: Clients can send and receive messages in real-time.
- **Error Handling**: Robust error handling for scenarios like invalid port numbers, invalid usernames, and connection failures.
- **Dynamic Client Handling**: The server can handle a dynamic number of clients, which is specified at runtime.
- **IP Address Display**: Displays the IP address of the connected clients for better traceability.

## How to Use

### Server

To start the server, compile and run the `server.cpp` file. You will be prompted to enter the maximum number of clients allowed. After entering the desired number, the server will start and wait for clients to connect.

```bash
$ g++ server.cpp -o server -lpthread
$ ./server [PORT_NUMBER]
```
### Client

To connect a client to the server, follow these steps:
1. Compile the `client.cpp` file using the following command:

    ```bash
    $ g++ client.cpp -o client -lpthread
    ```
2. Run the client with your desired username and the server's port number:

    ```bash
    $ ./client [USERNAME] [SERVER_PORT_NUMBER]
    ```
3. Once connected, you can start sending messages to other clients.

## Conclusion

This project demonstrates the power and versatility of socket programming in creating robust and real-time communication systems. Whether you are new to socket programming or seeking to gain insights into group chat dynamics, this project serves as a practical and informative guide.
