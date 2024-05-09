# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name : Iniyasri.S
## Register number : 212223230081
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## client
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## server
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())

```
## OUPUT
## client
![image](https://github.com/iniyasri4464/3b_CHAT_USING_TCP_SOCKETS/assets/152419072/3c83b57f-428e-424d-b558-4dee9a5ef167)
## server
![image](https://github.com/iniyasri4464/3b_CHAT_USING_TCP_SOCKETS/assets/152419072/291d44da-6ca8-4cd2-aa14-44880c00313d)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
