## TCP/IP

## What is TCP?
Transmission Control Protocol (TCP) is a communications standard that enable application programs to exchange data/messages
over a network. It purpose is to establishment of a connection between the sender and the receiver before data can be sent.

## How does it work? 
In order to have relyable transer of the data between devices, TCP use three way handshake, Let's take a client and server, first the client want to send a data to the server, so it send a SYN(Synchronize) to open the connection, second the serve receved the reuqest from the client and send ACK(Acknowledgment) accepting the connection request, third the client also send ACK(acknowledgment) confirming that it receved the response from the serve.

So, each side when sending a message the other side should send a response (ACK) to confirm that they have receved the message, using this method we confirm that the message is receved, and when we don't recved ACK we know that the message has faild.

Below image describe the three way handshake which TCP use.  
SYN, ACK, FIN
[IMAGE]


## Inside the TCP packet
The TCP packet contain the following fields:
- Data: The message that we want to send, it could be text, image, sound, etc.
- Protocol: The protocol that we use to send the message, we use TCP.
- Appliction Port: The application port number of the sender and receiver.
- IP Address: The IP address of the sender and the receiver. 
- MAC Address: The MAC address of the sender and the receiver.

> There're many application which enable us to capture the packets that are send in our network by using a packet analzyer tool, we will use Wireshark 

## TCP/IP Layers 
The TCP/IP layer describe the phases of sending and receving a message in the netowrk.
Each layer has its own specific function, on sending it use a encapsulation which each layer add its own header to the message, think about it as putting a message in a box, each layer adds another box to the preview box, 
While on the receiving side, the message is decapsulated, each layer remove its own header and pass the message, also you can think about it as opening the box, each layer open the box and pass the message to the next layer, until the message is receved to the application. 

[IMAGE]

TCP/IP
-   Application Layer: On the sending side the user intract with the application and send the message, while on the receiving side the message is viewed by the user.
-   Transport Layer: This layer add the header/box which protocol is used to send the message e.g. TCP or UDP. 
-   Network layer: This layer add the header/box which contain the IP address of the sender and the receiver. 
-   Data Link Layer: This layer add the header/box which contain the MAC address of the sender and the receiver.
-   Physical Layer: This layer is the hardware which send the message over the network.


> Think of the layer as a phases which should use to transfer the message, since the compuer will understand numbers, the message should convert to number in order to send it. 

