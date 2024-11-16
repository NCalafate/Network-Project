# Structured Computer Network Project

This repository contains documentation and configuration files for a structured computer network project, developed as part of the Computer Networks course in the Bachelor's Degree in Computer Engineering.

---

## Introduction
This project applies theoretical and practical knowledge to design and implement a structured computer network. It emphasizes hierarchical physical topology and structured cabling to ensure efficiency and reliability.

---

## Project Objectives
- Analyze functional areas and segment the network into subnets.
- Propose a suitable IP addressing scheme.
- Recommend appropriate cabling, passive, and active equipment.
- Define the location of equipment, outlets, and cable pathways.
- Configure active network devices.
- Design a logical network diagram.
- Provide a budget estimate.

---

## Location Description
- **RC Mobile Headquarters:** Hosts 30 permanent employees and provides public Wi-Fi access.
- **Additional Connections:** A branch office and warehouse located 20 km away, connected via fiber optics.

---

## Company Floor Plan
Below is the company floor plan. Each room's function is clearly labeled.

![image](https://github.com/user-attachments/assets/666c044c-243f-41b1-8f31-dcabafa25aed)


---

## Workstation Distribution
The distribution of workstations by room and function is as follows:

| Room | Function                           | Employees |
|------|------------------------------------|-----------|
| 1-4  | Software Development               | 8 (2 per room) |
| 5    | Archive and Supplies               | 1         |
| 6    | Administration Secretariat         | 1         |
| 7    | Administration                     | 2         |
| 8    | Treasury and Accounting            | 2         |
| 9    | Commercial                         | 2         |
| 10   | IT Support                         | 1         |
| 11-12| Microcontroller Systems Engineers  | 4 (2 per room) |
| 13-15| Integration Testing                | 8         |
| 16   | Telecommunications and Rack Room  | 1         |
| 17   | Meetings and Demonstrations        | 0         |
| 18   | Reception and Waiting Room         | 0         |
| 19   | Bar and Kitchen                    | 0         |
| 20   | Network Printer                    | 0         |

---

### Physical Network Topology

The image above illustrates the physical topology of the network for the RC Mobile headquarters. Here's a breakdown of the elements:

- **Green Square:** Server Room
- **Yellow Lines:** Represent the main cable paths used for backbone connections.
- **Blue Lines:** Indicate the structured cabling pathways for individual workstations and the vending machines (number 19).
- **Red Squares with Numbers:** Represent the network outlet points (RJ45 ports) within the building. Each number corresponds to a specific port in the structured cabling system.


![image](https://github.com/user-attachments/assets/47f496bd-5f58-4693-95a2-4cc62119c726)


---

## Wi-Fi Coverage
The building has full Wi-Fi coverage, ensured by two strategically placed access points.

![image](https://github.com/user-attachments/assets/2be6c433-d48c-43f3-b3aa-c126905cc92f)


---

## VLAN Identification
The network is segmented into VLANs based on department and function:

| VLAN ID | Function              |
|---------|-----------------------|
| 10      | Development           |
| 20      | Integration           |
| 30      | Microcontrollers      |
| 40      | Administration        |
| 50      | Archive               |
| 60      | Rack Room             |
| 70      | Commercial            |
| 80      | Accounting            |
| 90      | IT Support            |
| 100     | Secretariat           |
| 200     | IP Phones             |
| 300     | Vending Machines      |
| 400     | Printers              |
| 500     | Wi-Fi                 |
| 999     | Equipment Management  |

---

## Trunk Identification
Trunk connections between devices are configured as follows:

| Source        | Destination       | Ports          |
|---------------|-------------------|----------------|
| Router        | Switch 1          | F0/0 -> F0/1   |
| Switch 1      | Switch 2          | F0/5 -> F0/1   |
| Switch 1      | Switch 3          | F0/6 -> F0/1   |

---

## IP Addressing
The following table details the IP addressing plan:

| VLAN Name          | Hosts | Network IP    | Subnet Mask | IP Range              |
|---------------------|-------|---------------|-------------|-----------------------|
| IP Phones          | 62    | 192.168.10.0  | /26         | 192.168.10.1-62      |
| Wi-Fi              | 62    | 192.168.10.64 | /26         | 192.168.10.65-126    |
| Development        | 14    | 192.168.10.128| /28         | 192.168.10.129-142   |
| Integration        | 14    | 192.168.10.144| /28         | 192.168.10.145-158   |
| Microcontrollers   | 14    | 192.168.10.160| /28         | 192.168.10.161-174   |
| Administration     | 6     | 192.168.10.176| /29         | 192.168.10.177-182   |
| Archive            | 6     | 192.168.10.184| /29         | 192.168.10.185-190   |
| Rack Room          | 6     | 192.168.10.192| /29         | 192.168.10.193-198   |
| Commercial         | 6     | 192.168.10.200| /29         | 192.168.10.201-206   |
| Accounting         | 6     | 192.168.10.208| /29         | 192.168.10.209-214   |

---

## Network Rack (Bastidor)
The network rack contains:
- **1 Router:** CISCO1841
- **3 Switches:** WS-C2950-24
- **1 Server:** DELL PowerEdge R7515

---

### Budget (2022 Prices)

Below is the adjusted budget for the network project:

| Quantity | Equipment                                  | Total (€)      |
|----------|--------------------------------------------|----------------|
| 148      | Standard Cabling (32X16MM LEGRAND)         | €442.52        |
| 9        | T-Junction Cabling (32X16MM LEGRAND)       | €31.50         |
| 16       | Curved Cabling (32X16MM EFAPEL)            | €64.00         |
| 33       | Metal Cable Tray (60x200x3050MM RKSM 620FT)| €2,970.00      |
| 1        | Rack (48.26CM 32U, 600x1570x800MM)         | €1,088.86      |
| 3        | Switches (WS-C2950-24)                     | €2,747.13      |
| 1        | Router (CISCO1841)                         | €400.00        |
| 32       | Network Outlets (RJ45 80x80 2-5e UTP)      | €152.32        |
| 2        | Wi-Fi Access Points (AIR-AP1852I-E-K9)     | €1,344.72      |
| 1        | Server (DELL PowerEdge R7515)              | €3,584.86      |
| 20,000m  | Fiber Optic Cable                          | €13,245.65     |


The **total cost of the project** is **€26,071.56**, based on 2022 prices.

---

## Simulation in Packet Tracer
The network was simulated using **Cisco Packet Tracer**, configuring devices for VLANs, SSH, and DHCP.

![image](https://github.com/user-attachments/assets/306ba52b-f425-42ac-954b-4a6633a93e80)
![image](https://github.com/user-attachments/assets/8c37bf1c-2705-492e-9f7a-8fc6cc536fa3)



---

## Conclusions
The network infrastructure meets all the requirements, providing a functional and reliable solution for RC Mobile. This project enabled the practical application of theoretical concepts.

---

