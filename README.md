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
### Server Side
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
### Client Side
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```
## OUTPUT
![Chat using TCP Sockets](https://github.com/Aakashraj04/3b_CHAT_USING_TCP_SOCKETS/assets/121117266/5d2c3c90-4916-4f94-8446-93d36c4f84e1)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
