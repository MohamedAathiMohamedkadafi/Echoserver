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
```
client  :
import socket
HOST = "127.0.0.1" 
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Mohamed Aathil M ,212225040246")
    data = s.recv(1024)
print(f"Received {data!r}")

server :
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
```
## OUTPUT:
<img width="2172" height="563" alt="output" src="https://github.com/user-attachments/assets/0bf898f2-164a-4c51-9743-21f60cb4ae37" />

<img width="693" height="106" alt="image" src="https://github.com/user-attachments/assets/1ee80bb5-572f-4109-bb7f-611d14ab926b" />

Result:
The program is executed successfully
