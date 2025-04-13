# Design and Implementation of a Small Office Home Office Network 

## Scenario & Requirements:

XYZ company is a fast-growing company in Eastern Australia with more than 2 million customers globally. The company deals with selling and buying food items, which are basically operated by the headquarters. The company is intending to open a branch near the local village Bonalbo. Thus, the company requires young IT graduates to design the network for the branch. The network is intended to operate separately from the HQ network. Being a small network, the company has the following requirements regarding implementation:

•	One router and one switch to be used (all CISCO products).

•	3 departments (Admin/IT, Finance/HR and Customer service/Reception).

•	Each department is required to be in different VLANS.

•	Each department requires a wireless network for the users.

•	Host devices in the network are required to obtain IPv4 address automatically.

•	Devices in all the departments are required to communicate with each other.


Assume the ISP gave out a base network of 192.168.1.0, you as the young network engineer who has been hired, design and implement a network considering the above requirements.

## Technologies Implemented:
1.	Creating a Simple Network using a Router and Access Layer Switch.
2.	Connecting Networking devices with Correct cabling.
3.	Creating VLANs and assigning ports VLAN numbers.
4.	Subnetting and IP Addressing.
5.	Configuring Inter-VLAN Routing (Router on a stick).
6.	Configuring DHCP Server (Router as the DHCP Server).
7.	Configuring WLAN or wireless network (Cisco Access Point).
8.	Appling the ACLs
9.	Host Device Configurations.
10.	Test and Verifying Network Communication.


## Subnetting the network:

Base Network: 192.168.1.0

No. of subnets required: 3

No. of subnets = 2^n 

2^n=3   (n = number of bits borrowed)

2^2=4

Therefore: n = 2

Class C Address: 

255.255.255.0 = 11111111.11111111.11111111.00000000

Borrowing 2 bits from the host portion:

11111111.11111111.11111111.11000000 

New subnet mask: 255.255.255.192 OR /26

Block Size = 64

## Subnets:
#### 1st Subnet

Network ID: 192.168.1.0

Broadcast ID: 192.168.1.63

Host range: 192.168.1.1 - 192.168.1.62


#### 2nd Subnet

Network ID: 192.168.1.64

Broadcast ID: 192.168.1.127

Host range: 192.168.1.65 - 192.168.1.126


#### 3rd Subnet

Network ID: 192.168.1.128

Broadcast ID: 192.168.1.191

Host range: 192.168.1.129 - 192.168.1.190


#### 4th Subnet

Network ID: 192.168.1.192

Broadcast ID: 192.168.1.207

Host range: 192.168.1.193 - 192.168.1.206


## Network Layout:

![Soho-01](https://github.com/user-attachments/assets/d7533881-28af-42e7-84f3-806ae682c4dd)


 ## Configuration
Configuring VLANs on switch:

![Soho-02](https://github.com/user-attachments/assets/420870df-ff44-4107-a79f-7946a4cde229)

Basic configuration swith check connectivity:

![Soho-04](https://github.com/user-attachments/assets/a4146c36-c1fb-4de1-998a-f557c50641a6)

 Apllying ACLs:

![Soho-05](https://github.com/user-attachments/assets/54ab536c-0e47-47ea-817e-52fa5e8c856b)


Creating DHCP pools:

![Soho-03](https://github.com/user-attachments/assets/65711a77-ab39-4fc3-bbaf-094e7b4602ed)

Ensuring DHCP is successful:
 
Web Server:

![Soho-06](https://github.com/user-attachments/assets/26e996aa-e3f1-4fe2-8599-11cdccd699ec)


Email Server:

![Soho-07](https://github.com/user-attachments/assets/79fd27a1-4686-472f-b570-280fe76707d9)



