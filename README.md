## TCP/IP

## What is TCP?
Transmission Control Protocol (TCP) is a communications standard that enables application programs to exchange data/messages
over a network. Its purpose is to establish a connection between devices.

## How does it work? 
In order to have reliable transfer of data between devices, TCP uses a three-way handshake, Let's take a client and server, first, the client wants to send data to the server, so it sends a SYN(Synchronize) to open the connection, second the serve received the request from the client and send ACK(Acknowledgment) accepting the connection request, third the client also sends ACK(acknowledgment) confirming that it received the response from the serve.

So, on each side when sending a message the other side should send a response (ACK) to confirm that they have received the message, using this method we confirm that the message is received, and when we don't receive ACK we know that the message has failed.

Finally, to end the connection, the client sends FIN(Finish) to close the connection, and the server sends ACK to confirm that it received the request, and the server also sends FIN to close the connection, and the client sends ACK to confirm that it received the request.

![syn-ack-fin](https://github.com/user-attachments/assets/40c3a072-ec9a-48ed-8bf8-498e6f0f9106)

## Inside the TCP packet
The TCP packet contains the following fields:
- Data: The message that we want to send, could be text, image, sound, etc.
- Protocol: The protocol that we use to send the message, we use TCP.
- Application Port: The application port number of the sender and receiver.
- IP Address: The IP address of the sender and the receiver. 
- MAC Address: The MAC address of the sender and the receiver.

![frame](https://github.com/user-attachments/assets/06884152-f42d-4032-9ffb-c07346b18dbe)

> We can see the packets that have been transferred in our networking by using the packet analysis tool as **Wireshark**
> There are many applications that enable us to capture the packets that are sent in our network by using a packet analysis tool, we will use Wireshark 

## TCP/IP Layers 
The TCP/IP layer describes the phases of sending and receiving a message in the network.
Each layer has its own specific function, on sending it use an encapsulation in which each layer adds its own header to the message, think about it as putting a message in a box, each layer adds another box to the preview box, 
While on the receiving side, the message is decapsulated, each layer removes its own header and passes the message, also you can think about it as opening the box, each layer opens the box and passes the message to the next layer until the message is received to the application. 

![osi-model](https://github.com/user-attachments/assets/9b5abf87-a6b2-4bf5-bbe8-3ba3ac2fb072)

TCP/IP
-   Application Layer: On the sending side the user interacts with the application and sends the message, while on the receiving side, the message is viewed by the user.
-   Transport Layer: This layer adds the header/box in which protocol is used to send the message e.g. TCP or UDP. 
-   Network layer: This layer adds the header/box which contains the IP address of the sender and the receiver. 
-   Data Link Layer: This layer adds the header/box which contains the MAC address of the sender and the receiver.
-   Physical Layer: This layer is the hardware that sends the message over the network.


> Think of the layers as phases that should be used to transfer the message, since the computer will understand numbers, the message should convert to numbers in order to send it. 
