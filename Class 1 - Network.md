# Software Systems 

An application process running on a network needs to open a socket to the transport layer protocol,
either UDP or TCP, to begin communication with another application process somewhere else on the
network. The purpose of this class is to get some hands-on experience of socket programming, in order
to help us better understand the application and transport layer concepts which will be covered in
future lectures. 

## Task 1 

<img width="555" alt="Screenshot 2022-11-01 at 09 44 59" src="https://user-images.githubusercontent.com/115703122/199205905-91ae05fd-7354-484f-9238-ebe4c46c3db3.png">

OUTPUT FROM TERMINAL:

<img width="477" alt="Screenshot 2022-11-01 at 09 45 46" src="https://user-images.githubusercontent.com/115703122/199206028-1e441c4f-fac6-4e3e-90cd-00e1cb3a37b7.png">

UDP CLIENT:

<img width="554" alt="Screenshot 2022-11-01 at 09 46 02" src="https://user-images.githubusercontent.com/115703122/199206086-640a77dd-5209-444e-b902-373dcb868ab8.png">

OUTPUT FROM TERMINAL:

<img width="509" alt="Screenshot 2022-11-01 at 09 46 27" src="https://user-images.githubusercontent.com/115703122/199206137-6d91d1a7-0cbc-4aa0-a0d7-69a05332b9fe.png">

TCP Output (the same as udp):

<img width="465" alt="Screenshot 2022-11-01 at 10 06 06" src="https://user-images.githubusercontent.com/115703122/199209612-d719fb08-9f8e-4995-a0ee-81bc82b2e026.png">

Modified code so that instead of finding alphanumeric to now enter a message from the client and print in the server:

<img width="352" alt="Screenshot 2022-11-01 at 10 09 27" src="https://user-images.githubusercontent.com/115703122/199210208-b96ee2d4-ea33-4b20-b4db-ccce660c5c9d.png">

<img width="578" alt="Screenshot 2022-11-01 at 10 10 16" src="https://user-images.githubusercontent.com/115703122/199210366-9e924370-9aec-4665-84e7-60662a6f3cee.png">

OUTPUT:

<img width="479" alt="Screenshot 2022-11-01 at 10 10 36" src="https://user-images.githubusercontent.com/115703122/199210432-b4c275bd-a505-468e-bc77-0d4394390550.png">


## Task 2 

Move the client and server processes to two different computers. We will assume that these
computers are in the same LAN, e.g., two laptops currently present in your classroom, both
connected to the college Wi-Fi.

We need to incorporate the following change in the UDP client:
Instead of sending the message to localhost, the client sends it to the IPv4 address of the server.
To see this address, on the server computer open command prompt and execute ipconfig. You
should see the 32-bit IPv4 IP address as show below

<img width="484" alt="Screenshot 2022-11-01 at 10 20 16" src="https://user-images.githubusercontent.com/115703122/199212141-3932c8b2-977d-4039-832d-b519eb9e2fe7.png">

I then changed my server IP from my TCPClient to a different laptopns IP, after they ran server i was able to communicate by running client by running client and reciving the response from a server with a different IP:

<img width="478" alt="Screenshot 2022-11-01 at 10 21 59" src="https://user-images.githubusercontent.com/115703122/199212437-3b3ebf8b-8085-4a52-bc8e-8c5da79468e2.png">


## Task 3 

In this exercise, we will run two client processes, both of which talk to a single server process.
Create two UDP clients, c1 and c2. Bind c1 to port 11000 and c2 to port 13000.
The server should run on port 12000.
Write code in both c1 and c2 to repeatedly send messages to the server. The messages should be
numbers between 1 and 100, sent in sequence, rolling back to 1 after 100. So the clients are
infinite loops sending these messages to the server. Add a small amount of delay in the loops so
that the processes can be observed easily. You can use time.sleep(value) to add delay.

The server should accept messages from c1 and c2, and simply print which message was sent by
which client. It should print the messages in the order they were received in.
The server will need to distinguish between the two clients. If all three processes are running on
the same computer, they have the same IP numbers, so the port number will be needed to
distinguish them. You can access the port number from the caddr variable, which is an array
containing the IP and port number of the client at caddr[0] and caddr[1] respectively.

<img width="617" alt="Screenshot 2022-11-01 at 11 26 19" src="https://user-images.githubusercontent.com/115703122/199222760-0225921b-f5cb-486b-a19a-d67e6cc99c11.png">

<img width="611" alt="Screenshot 2022-11-01 at 11 26 34" src="https://user-images.githubusercontent.com/115703122/199222794-011deb7f-3e4e-45ea-87a6-7525af894a95.png">

<img width="635" alt="Screenshot 2022-11-01 at 11 26 46" src="https://user-images.githubusercontent.com/115703122/199222822-11484b04-4693-4ccc-8b46-0afe6cee6f4f.png">

<img width="452" alt="Screenshot 2022-11-01 at 11 27 02" src="https://user-images.githubusercontent.com/115703122/199222859-3ff94b17-9434-4b7e-9865-1433c0473ca2.png">


