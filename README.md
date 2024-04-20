# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## SERVER:
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
## OUPUT:
## CLIENT:
<img width="439" alt="Screenshot 2024-04-20 233507" src="https://github.com/Keerthana-VJ/3b_CHAT_USING_TCP_SOCKETS/assets/149347704/bc5da1e0-aaeb-4ebc-9517-a1c5c741e68e">

## SERVER:
<img width="438" alt="Screenshot 2024-04-20 233521" src="https://github.com/Keerthana-VJ/3b_CHAT_USING_TCP_SOCKETS/assets/149347704/9a4ac5ed-2f70-4a01-88c2-0dcfd9d3736e">

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
