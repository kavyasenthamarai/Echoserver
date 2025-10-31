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
## Server.py
```
import socket
HOST = "127.0.0.1"
PORT = 65432
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
## client.py
```
import socket
HOST = "127.0.0.1"
PORT = 65432
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
s.connect((HOST, PORT))
s.sendall(b"Hello, world")
data = s.recv(1024)
print(f"Received {data!r}")
```
## OUTPUT:
<img width="1237" height="768" alt="Screenshot 2025-10-31 142128" src="https://github.com/user-attachments/assets/8aad4873-4bc1-43e3-8814-58173756117a" />

## RESULT:
The program is executed successfully
