# 2b IMPLEMENTATION OF SLIDING WINDOW PROTOCOL

## AIM
To write a python program to perform sliding window protocol
## ALGORITHM:
STEP 1
Read the given Data
STEP 2
Get the information about the data
STEP 3
Remove the null values from the data
STEP 4
Save the Clean data to the file
STEP 5
Remove outliers using IQR
STEP 6
Use zscore of to remove outliers
## PROGRAM:
DEVELOPED BY : SHANMUGA RAJ.K
REG NO : 212223040192
### Client:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
size=int(input("Enter number of frames to send : "))
l=list(range(size))
s=int(input("Enter Window Size : "))
st=0
i=0
while True:
 while(i<len(l)):
  st+=s
  c.send(str(l[i:st]).encode())
  ack=c.recv(1024).decode()
   if ack:
   print(ack)
   i+=s
```
### Server:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True: 
 print(s.recv(1024).decode())
 s.send("acknowledgement recived from the server".encode())
```
## OUPUT
![Screenshot (137)](https://github.com/K-Shanmugaraj/2b_SLIDING_WINDOW_PROTOCOL/assets/144870425/cdab857b-1910-463b-be4a-52c0c8086a9d)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed
