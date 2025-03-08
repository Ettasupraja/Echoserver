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

client:
![WhatsApp Image 2025-03-06 at 06 16 04_853f67d4](https://github.com/user-attachments/assets/0aedc355-423e-4468-b813-8ae1761af84e)

server:
![WhatsApp Image 2025-03-06 at 06 16 26_e172e679](https://github.com/user-attachments/assets/25a419b7-2e50-4eeb-9bb7-8a0e533bfe97)



## RESULT:
The program is executed successfully
