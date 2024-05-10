# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## Name:Sanjev R M
## REG NO:212223040186
# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
### client:
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### server:
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
``` 
## OUPUT
### client:
![image](https://github.com/sanjevrm/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/155142423/751764da-a4ca-48c5-9d58-ab44dda66b8f)


### server:
![image](https://github.com/sanjevrm/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/155142423/1022d394-a99e-4bb0-8de3-00b44eb4be9f)




## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
