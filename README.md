# 2a_Stop_and_Wait_Protocol
## AIM :
To write a python program to perform stop and wait protocol
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
DEVELOPED BY:GOKHULRAJ V

REG NO:212223230064
# CLIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break
```
# SERVER:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT
# CLIENT:
![Screenshot 2024-04-16 185034](https://github.com/RENUGASARAVANAN/2a_Stop_and_Wait_Protocol/assets/119292258/b05ccdd2-b8b1-42fb-b8bf-4b42f5dda211)

# SERVER:
![Screenshot 2024-04-16 185052](https://github.com/RENUGASARAVANAN/2a_Stop_and_Wait_Protocol/assets/119292258/7508e4c6-8c45-4e65-8595-12ece38c8768)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
