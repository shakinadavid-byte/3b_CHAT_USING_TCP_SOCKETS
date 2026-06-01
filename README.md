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
SERVER.PY:
```
import socket 
s=socket.socket() 
s.bind(('localhost',8080)) 
s.listen(5) 
c,addr=s.accept()
while True: 
    ClientMessage=c.recv(1024).decode() 
    print("Client > ",ClientMessage) 
    msg=input("Server > ") 
    c.send(msg.encode())
```
CLIENT.PY:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8080)) 
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUTPUT:

<img width="1849" height="962" alt="Screenshot 2026-05-23 192637" src="https://github.com/user-attachments/assets/fbfbad69-06cf-44b5-a108-e47b197cba29" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
