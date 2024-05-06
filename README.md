# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
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


client:

```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
clientMessage=c.recv(1024).decode()
c.send((clientMessage.encode()))
```


server:


```

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
msg=input("client>")
s.send(msg.encode())
print("server>",s.recv(1024).decode())


```


## OUPUT


client:


![image](https://github.com/Mythili7339267708/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144260246/8fed98c5-f768-47e9-9e8d-c318be73514b)




server:



![image](https://github.com/Mythili7339267708/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/144260246/e356d4b8-eb3e-430d-b097-e959fd489ee5)




## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
