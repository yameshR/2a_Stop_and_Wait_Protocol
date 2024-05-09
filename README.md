# 2a_Stop_and_Wait_Protocol
## Name:Yamesh R
## REG NO:212222220059
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
# CLIENT:
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

## SERVER
import socket   
s=socket.socket()   
s.connect(('localhost',8000))   
while True:   
print(s.recv(1024).decode())   
s.send("Acknowledgement Recived".encode())   

# OUTPUT
## CLIENT:
![Screenshot 2024-04-09 152419](https://github.com/23004513/SocketStudy/assets/138973069/ba59b22b-cfb8-4552-af79-7e00532e353e)

## SERVER:
![Screenshot 2024-04-09 152432](https://github.com/23004513/SocketStudy/assets/138973069/d4b0944c-e6b0-457e-b090-2f6b882b9150)


# Result:
Thus python program to perform stop and wait protocol was successfully executed.
