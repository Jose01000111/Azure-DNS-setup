## Azure DNS 🧪 Lab: Setup and Exploration 🚀

<p align="center">
  <img src="https://github.com/user-attachments/assets/0866896c-df33-43b2-b439-fa973e589a69" alt="r79LEht" />
</p>

#### I built this 🌐 DNS lab to get hands-on practice with DNS concepts ahead of my CompTIA A+ exam certification. Setting up and querying DNS servers helped me understand how name resolution works and prepared me for real-world troubleshooting.

### Part 1: Setting Up Azure Virtual Machines 🖥️
I started by creating two Azure VMs in the same resource group and virtual network for easy communication. The first VM is a Linux server (dns-linux-lab-vm) that will eventually host the DNS server software BIND9. The second VM is a Windows client (win-client-lab-vm) that I will use to simulate DNS client queries and test responses. I made sure to open SSH (port 22) on the Linux VM and RDP (port 3389) on the Windows VM so I can connect to them remotely.

![SkwWDSC](https://github.com/user-attachments/assets/79727582-4d9e-47c6-8489-18a783ab275e)

![jNt1XGl](https://github.com/user-attachments/assets/d621bc49-a5d3-4aeb-b34c-dd5d8fb93f53)

![SrJMPOk](https://github.com/user-attachments/assets/4536c59e-4534-4be0-b167-b92739b4b10a)

![fUfK4D8](https://github.com/user-attachments/assets/3a5134f7-c097-4541-89e3-c0fe409dc997)

![Bl4K3U3](https://github.com/user-attachments/assets/88aed682-b25e-4dae-b9da-1e11a7575ddb)

### Part 2: Connecting to My VMs 🔐
Once both VMs were up and running, I connected to the Linux server via SSH using the username azureuser and the IP address 20.80.104.60. For the Windows client, I used Remote Desktop to connect with the username JGadmin and IP 20.221.58.49. Having access to both machines allowed me to start configuring tools and testing DNS queries between them.





### Part 3: Installing DNS Utilities on Linux and Testing 🧰
On the Linux VM, I installed essential DNS utilities like dig, host, and nslookup to perform DNS lookups from the command line. These tools helped me query public DNS servers and understand how DNS resolution works in practice. For example, I used dig google.com to see detailed DNS response data and learned how to read the answers, authority, and additional sections in the output.



### Part 4: Querying Non-Existent DNS Records and Understanding Errors 🔍
Since I hadn’t set up any DNS zones yet, I experimented by querying DNS records that don’t exist on my local DNS server using dig. This helped me observe common DNS errors like NXDOMAIN (domain not found), SERVFAIL (server failure), and REFUSED (query refused). These error messages gave me valuable insight into DNS troubleshooting and what happens when a DNS server cannot resolve a query.



### What I Learned 📚
How to set up and connect to Azure VMs securely via SSH and RDP.

The basics of DNS queries and responses using command-line utilities.

Different DNS error codes and what they mean for troubleshooting.

How a client and DNS server interact in a networked environment.

### Tech Stack 🛠️
Azure (VM provisioning, networking)

Linux Ubuntu Server (DNS server host)

Windows 10/11 (client testing)

BIND9 (planned DNS server software)

DNS Utilities: dig, host, nslookup

Protocols: DNS, SSH, RDP

### Goals Accomplished ✅
Successfully deployed Linux and Windows VMs in Azure within the same network.

Connected to both VMs securely and prepared the environment for DNS configuration.

Installed and used DNS query tools to perform and analyze DNS lookups.

Gained hands-on understanding of DNS error handling and query troubleshooting.

