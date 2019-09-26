tcp connection 3 way hand shake.txt

Most of you guys already know that Transmission Control Protocol is its full form. Now lets understand what infact is Transmission Control Protocol.
The name do indicate us that it is something that controls the transmission of the data in a reliable manner.
lets understand when and where does the TCP comes into play when two machines in network communicate with each other.

Every operating system currently available in the market be it Windows,Linux,Mac,Unix or Even the Mobile operating systems like Symbian,Android,Ios etc all comes
packed with the tcp stack in them. Without the operating system's kernel having the TCP network stack inbuilt into them there is no possibility that communication can
happen between that device and others.
TCP stack consists of the following things. The contents on the TCP stack exists in Layers and they are as the following.

Different Layers of TCP

Layer 5: This is the layer from where our applications tries to establish connection to a server. For example imagine that you have Firefox Browser installed
on your machine, and you are trying to establish connection with www.google.com. Now the Browser knows how to open a temporary port and request a connection to 80 port
on www.google.com server.This layer is called as the application Layer, where all our applications try to establish connections. Be it a browser,ftp client,ssh client
etc.

Layer 4: This is the layer where our topic comes into picture, this layer is named as Transport Layer, There are two protocols in this layer(TCP,UDP). Either of them
can be used, Mostly in our day to day life we use TCP(because most of the applications require a reliable connection which TCP provides).UDP is also used for example,
in order to query a DNS server we normally use UDP protocol. Most of you must have heard about segments in network or MSS (Maximum Segment Size), Now TCP provides
reliability in communication with the help of something called as Positive Acknowledgment with Re-transmission (PAR).

Now a system using PAR resends the data unless it gets an acknowledgement that the data arrived at destination is okay.The chunks of data in transport layer
is called segments. Each segment that a machine sends also contains a checksum which checks whether the data recieved at recievers end is correct. If the data recieved
at the recievers end is undamaged, then the reciever sends a positive acknowledgement, and if it is damaged, then the reciver discards that segment(and the sender
resends all the segments for which positive acknowledgement is not recieved).

Now there is an important question.Why is three way Handshake called as three way handshake??????????

Because three segments are exchanged between the sender and reciever for a reliable TCP connection to get established.

TCP handshake

I will explain all the three above mentioned steps in detail one by one.

Step1: Machine 1 wants to initiate a connection with machine 2, So machine 1 sends a segment with SYN(Synchronize Sequence Number). This segment will inform the machine 2 that Machine 1 would like to start a communication with Machine 2 and informs machine 2 what sequence number it will start its segments with.

Note: Sequence Numbers are mainly used to keep data in order.

Step2: Machine 2 will respond to Machine 1 with "Acknowledgment" (ACK) and SYN bits set. Now machine 2's ACK segment does two things; they are as below.

1. It acknowledges machine 1's SYN segment.

2.It informs Machine 1 what sequence number it will start its data with.

 

Step 3:Now finally machine 1 Acknowledges Machine 2's initial sequence Number and its ACK signal. And then Machine 1 will start the actual data transffer.

 

Note: Initial Sequence Numbers are randomly selected while initiating connections between two machines.
