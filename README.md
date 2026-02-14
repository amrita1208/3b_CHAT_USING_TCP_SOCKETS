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
## client:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## server:
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
<img width="1555" height="922" alt="Screenshot 2026-02-14 113936" src="https://github.com/user-attachments/assets/4a4f62d3-0a1f-45ac-b53e-c47be2582194" />

<img width="1556" height="913" alt="image" src="https://github.com/user-attachments/assets/6e410e73-d2b8-410f-bda9-1a82d542f9ab" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
