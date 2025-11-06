
# 👋 Hi, I'm Abhishek More 

**Data Science & Full Stack Developer**<br><br>
🌐 Explore My Portfolio : [abhimore.netlify.app](https://abhimore.netlify.app/) <br>
A living canvas of my projects, capabilities, and innovations.

---



## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment


---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

_Simplicity is the ultimate sophistication._

## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment

---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

_Simplicity is the ultimate sophistication._ 

import socket
import os

# Server details
server_ip = "127.0.0.1"   # Change to server’s LAN IP for two-machine setup
server_port = 5005

client_socket = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)

filename = input("Enter the file name to send: ")

if not os.path.exists(filename):
    print("❌ File not found!")
    exit()

# Send filename first
client_socket.sendto(filename.encode(), (server_ip, server_port))

# Send file data
with open(filename, "rb") as f:
    while True:
        data = f.read(4096)
        if not data:
            break
        client_socket.sendto(data, (server_ip, server_port))

# Send end-of-file marker
client_socket.sendto(b"EOF", (server_ip, server_port))

print("✅ File sent successfully.")
client_socket.close()

#udp_server.py


import socket
import os

# Server details
host = "0.0.0.0"   # Listen on all interfaces
port = 5005

# Create UDP socket
server_socket = socket.socket(socket.AF_INET, socket.SOCK_DGRAM)
server_socket.bind((host, port))

print(f"UDP Server listening on {host}:{port}")

# Receive filename first
filename, addr = server_socket.recvfrom(1024)
filename = filename.decode()
print(f"Receiving file: {filename} from {addr}")

# Open file for writing in binary mode
with open("received_" + filename, "wb") as f:
    while True:
        data, addr = server_socket.recvfrom(4096)
        if data == b"EOF":  # End of file marker
            print("File transfer completed.")
            break
        f.write(data)

server_socket.close()
print("Connection closed.")
