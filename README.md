# EX-2 IMPLEMENTATION OF STOP AND WAIT PROTOCOL

## DATE: 13/03/23

## AIM :

To write a python program to perform stop and wait protocol

## ALGORITHM :

1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
otherwise it will sendNACK signal to client.
6. Stop the program


## PROGRAM :

### client:
```python
Developed by : Tejusve Kabeer.F
Register no : 212222100054

import socket
s=socket.socket()
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

### server:
```python
Developed by : Tejusve Kabeer.F
Register no : 212222100054

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
 s.bind(('localhost',8000))
```

## OUTPUT :

### clientoutput:
![1aco](https://github.com/Reebak04/EX-2/assets/118364993/9d0082ee-c43d-4002-b923-729fa824f277)

### serveroutput:
![1aso](https://github.com/Reebak04/EX-2/assets/118364993/407773cf-fbc6-4895-a3f7-0629e40e6152)

## RESULT :

Thus, python program to perform stop and wait protocol was successfully executed.


