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

Server side
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
Client side
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())

```
## OUPUT
Server side
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1f40e416-8d4e-4472-b69e-7b9deb285256" />
Client side 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/defe8b2b-b38e-45bf-95c0-ca25f6f517a6" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
