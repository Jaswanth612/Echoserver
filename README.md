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
## server.py
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_server((HOST, PORT)) as s:
    conn, addr = s.accept()
    with conn:
        print(f'Connected by {addr}')
        while data := conn.recv(1024):
            conn.sendall(data)
```
## client.py
```
import socket
HOST, PORT = '127.0.0.1', 65432
with socket.create_connection((HOST, PORT)) as s:
    s.sendall(b'JASWANTH S., 212223220037')
    print(f'Received: {s.recv(1024)!r}')
```



## OUTPUT:

![Screenshot 2025-03-06 112915](https://github.com/user-attachments/assets/32f3e255-e084-4528-b3ec-147b5d5eeab4)


## RESULT:
The program is executed successfully
