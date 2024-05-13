# 3b.CREATION FOR CHAT USING TCP SOCKETS
## NAME: KARTHIKEYAN R
## REG.NO:212222240046
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
## Client:
![client output](https://github.com/AnnaLahari/3b_CHAT_USING_TCP_SOCKETS/assets/149365425/047ce11a-a4d7-4371-a1fb-2c4d62fec59d)
## Server:
![server output](https://github.com/AnnaLahari/3b_CHAT_USING_TCP_SOCKETS/assets/149365425/b9ecce04-e616-4ac9-8e6f-af7939cca60d)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
