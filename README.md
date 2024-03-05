# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:

## Echo Client.py

import socket

HOST = "127.0.0.1"  # Standard loopback interface address (localhost)

PORT = 65432  # Port to listen on (non-privileged ports are > 1023)

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:

    s.bind((HOST, PORT))
    
    s.listen()
    
    conn, addr = s.accept()
    
    with conn:
    
        print(f"Connected by {addr}")
        
        while True:
        
            data = conn.recv(1024)
            
            if not data:
            
                break
                
            conn.sendall(data)

## Echo Server.py
import socket

HOST = "127.0.0.1"  # Standard loopback interface address (localhost)

PORT = 65432  # Port to listen on (non-privileged ports are > 1023)

with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:

    s.bind((HOST, PORT))
    
    s.listen()
    
    conn, addr = s.accept()
    
    with conn:
    
        print(f"Connected by {addr}")
        
        while True:
        
            data = conn.recv(1024)
            
            if not data:
            
                break
                
            conn.sendall(data)
            
## OUTPUT:
## Client
![image](https://github.com/LakshmanAdhireddy/Echoserver/assets/118707265/f9cbf8ac-258e-4fa2-b516-23340fc36f4b)

## Server
![image](https://github.com/LakshmanAdhireddy/Echoserver/assets/118707265/2d06b344-f529-4cc1-86d5-beaf40832e92)

## RESULT:
The program is executed successfully
