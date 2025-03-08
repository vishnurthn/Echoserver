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
Client :
import socket


HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server


with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"VISHNU RATHAN B , 212224240185 ")
    data = s.recv(1024)


print(f"Received {data!r}")

Server :
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

![Screenshot 2025-03-08 130315](https://github.com/user-attachments/assets/a757e799-a403-4a9e-86e3-7390056c221f)

![Screenshot 2025-03-08 125655](https://github.com/user-attachments/assets/9d6097db-860a-4a68-a2e2-dcc7f6da2153)

## RESULT:
The program is executed successfully
