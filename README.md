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

client:
```
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Etta supraja,212223220022 06-03-2025")
    data = s.recv(1024)


print(f"Received {data!r}")

```
server:
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

## OUTPUT:
client :

![WhatsApp Image 2025-03-06 at 06 16 04_8e89cffa](https://github.com/user-attachments/assets/d9978252-4a04-47bc-81b5-0e158e5ec7a3)

server:
![WhatsApp Image 2025-03-06 at 06 16 26_5b4faa43](https://github.com/user-attachments/assets/18361903-b4ac-4b2a-88bf-552007e56055)


## RESULT:
The program is executed successfully
