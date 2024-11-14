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
```py
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
```py
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
msg=input("Client > ")
s.send(msg.encode())
print("Server > ",s.recv(1024).decode())
```
## OUPUT
### SERVER
![WhatsApp Image 2024-11-14 at 11 09 11_a5d64248](https://github.com/user-attachments/assets/bf015090-4eab-4336-b370-fdae54ef3d79)


### CLIENT
![WhatsApp Image 2024-11-14 at 11 08 32_883048ff](https://github.com/user-attachments/assets/005bf654-3882-487f-8975-2d49efdfde06)


## RESULT

Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
