# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER

### DATE :03-05-2023

### AIM :
## To write a python program for creating Chat using TCP Sockets Links.

### ALGORITHM :
### Client:

## 1.Import the necessary modules in python
## 2.reate a socket connection to using the socket module.
## 3.Send message to the client and receive the message from the client using the Socket module in server
## 4.Send and receive the message using the send function in socket.

### PROGRAM :
### CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```   
### SERVER:
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
### CLIENT OUTPUT :
![image](https://github.com/tsanjaithirumal/EX-9/assets/119393916/80a293c9-b113-415e-8d76-2191bb9fde76)

### SERVER OUTPUT :
![image](https://github.com/tsanjaithirumal/EX-9/assets/119393916/d0ef6dd5-251e-4a07-9f21-b1e6e75ccabd)



### RESULT :
## Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
