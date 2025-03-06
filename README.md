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
![Screenshot 2025-03-06 115257](https://github.com/user-attachments/assets/db4602ac-0dd3-428d-ba76-5cf01aea33a9)
![Screenshot 2025-03-06 115414](https://github.com/user-attachments/assets/bee285ef-5362-4121-b7d5-8811109f0f79)




## RESULT:
The program is executed successfully
