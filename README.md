# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### Client:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server:
```python
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
### Client:
![Screenshot 2024-04-03 154855](https://github.com/Raja8334/3b_CHAT_USING_TCP_SOCKETS/assets/120719634/765d572a-1b1f-4311-802f-91676b164498)
### Server:
![Screenshot 2024-04-03 154907](https://github.com/Raja8334/3b_CHAT_USING_TCP_SOCKETS/assets/120719634/5f9334bf-96b9-46b8-ac00-12c5759ae68f)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
