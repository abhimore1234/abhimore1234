
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




## nano terminal

Program statement : . Installing and configuring DHCP server and assign IP addresses to client 
machines using DHCP server. 

Commands : 
1. sudo apt update 
2. sudo apt install isc-dhcp-server 
3. sudo nano /etc/dhcp/dhcpd.conf 
default-lease-time 600;
max-lease-time 7200;
option domain-name "example.com";
option domain-name-servers 8.8.8.8, 8.8.4.4;

 
subnet 172.16.0.0 netmask 255.255.0.0 { 
range 172.16.3.100 172.16.3.200; option 
routers 172.16.3.1; option broadcast
address 172.16.255.255; 
} 
4. sudo 
nano 
/etc/default/isc-dhcp-server 
INTERFACESv4="enp1s0" or "eth0"
5. sudo systemctl restart isc-dhcp-server 
6. sudo systemctl status isc-dhcp-server 



}

## code 

import socket 
 
def dns_lookup(): 
    print("=== DNS Lookup Tool ===") 
    print("1. URL → IP address") 
    print("2. IP address → URL") 
     
    choice = input("Enter your choice (1 or 2): ") 
 
    if choice == "1": 
        # Hostname to IP 
        hostname = input("Enter website URL (e.g. www.google.com): ") 
        try: 
            ip = socket.gethostbyname(hostname) 
            print(f"IP address of {hostname} is: {ip}") 
        except socket.gaierror: 
            print("❌ Invalid hostname or network issue.") 
 
    elif choice == "2": 
        # IP to Hostname 
        ip_address = input("Enter IP address (e.g. 8.8.8.8): ") 
        try: 
            host = socket.gethostbyaddr(ip_address) 
            print(f"Hostname for IP {ip_address} is: {host[0]}") 
        except socket.herror: 
            print("❌ Hostname not found for this IP address.") 
 
    else: 
        print("Invalid choice! Please enter 1 or 2.") 
 
if __name__ == "__main__": 
    dns_lookup()
