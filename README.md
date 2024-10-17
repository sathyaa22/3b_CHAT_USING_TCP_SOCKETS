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

### client:
```import socket 
s=socket.socket() 
s.connect(('localhost',8080)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```

### server:
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

## OUPUT

### client:

![client3](https://github.com/user-attachments/assets/cb6cc739-bf77-4f54-98cd-c1374ff69a8b)

### server:

![server3](https://github.com/user-attachments/assets/fed467b0-658d-4cf1-b18f-81a202e93e85)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
