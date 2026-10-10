# CyberDefenders – PsExec Hunt

## About the Lab

This was a network forensics lab on CyberDefenders where I investigated a PCAP file using Wireshark. The goal was to analyze network traffic, identify systems involved in the attack, and understand how the attacker moved between machines in the network.

## Tools Used
- Wireshark
- CyberDefenders lab environment
- PCAP network capture

## What I Did

My Activities
Through this lab, I:

- Examined captured network packets using Wireshark tool.
- Explored SMB communication to learn about its behavior.
- Filtered packets to focus on relevant traffic of my interest.
- Tracked TCP streams in order to understand the communication better.
- Studied NTLMSSP authentication packets to learn more about the machine.
- Attempted to find evidence indicating lateral movements.

## Key Findings

- Attacker's entry machine: 10.0.0.130
- Initial SMB target: 10.0.0.133
- First pivot machine: Sales-PC
- Authentication username: ssales
- Service executable: psexesvc.exe
- Second pivot machine: MARKETING-PC


## Tasks and Answers

### Q1. Attacker's Initial IP Address
**Question:** What is the IP address of the machine from which the attacker initially gained access?

**Answer:** `10.0.0.130`

### Q2. First Pivot Machine
**Question:** What is the hostname of the machine to which the attacker first pivoted?

**Answer:** `Sales-PC`

### Q3. Attacker's Username
**Question:** What username did the attacker use for authentication?

**Answer:** `ssales`

### Q4. Service Executable
**Question:** What service executable did the attacker set up on the target machine?

**Answer:** `psexesvc.exe`

### Q5. Service Installation Share
**Question:** Which network share did PsExec use to install the service on the target machine?

**Answer:** `ADMIN$`

### Q6. PsExec Communication Share
**Question:** Which network share did PsExec use for communication between the machines?

**Answer:** `IPC$`

### Q7. Second Pivot Machine
**Question:** What is the hostname of the second machine the attacker targeted for further lateral movement?

**Answer:** `MARKETING-PC`


## What I Learned

This lab helped me get more comfortable using Wireshark to investigate network traffic. I also learned how to follow TCP streams, examine SMB communication, and find useful information in authentication traffic.

One of the main things I learned was that packet captures can reveal details about communication between machines and help an investigator understand possible lateral movement.

## Screenshots

I included well-labelled screenshots of the tasks solved in the `screenshots` folder.

## Repository Structure
```text
CyberLabs SOC-L1-PsExec-Hunt/
├── README.md
└── screenshots/
    ├── task-1-attacker-ip.png
    ├── task-2-smb-target.png
    ├── task-3-psexec-traffic.png
    ├── task-4-network-investigation.png
    ├── task-5-authentication-analysis.png
    ├── task-6-lateral-movement.png
    └── task-7-marketing-pc.png
```

## Connect

Thank you for taking the time to view this project.

I'm documenting my cybersecurity learning journey by completing hands-on labs in networking, Linux, digital forensics, cloud computing, and SOC analysis. Feel free to explore my other repositories to see what I'm learning next.

[![GitHub](https://img.shields.io/badge/GitHub-mohamedbrek-181717?logo=github)](https://github.com/mohamedbrek)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mohamed%20Brek-0A66C2?logo=linkedin)](https://linkedin.com/in/mohamed-brek-9130a6411)
