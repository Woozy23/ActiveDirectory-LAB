# ActiveDirectory-LAB


Title: Active Directory Lab: Multi-Client Domain Environment

Overview

Designed and deployed a Windows Server 2022 Domain Controller in a Virtualbox environment, after I configured Active Directory DNS, and Group Policy, and joined multiple Windows 10 pro client machines to the domain. I created users, groups, and applied GPOs to enforce security policies and manage access.


Architecture

- DC: Windows Server 2022 (Active Directory and DNS)
- Client: Windows 10 Pro
- Network: Virtual Internal Network and NAT for internet


![Untitled Diagram](https://github.com/user-attachments/assets/bc0bcede-8241-445e-9297-74578f987cbf)


Steps Taken

- Installed Windows Server 2022 and promoted to Domain controller
- Configured DNS for domain lab.trial
- Created Organizational Units
- Added users and groups inside OUs
- Applied Group Policies (ex: enforcing password rules and restricting access to various settings)
- Joined multiple client VMs to the domain
- Verified policies and login authentication


<img width="2563" height="1440" alt="Screenshot (3)" src="https://github.com/user-attachments/assets/d7be08d2-7a58-42f3-8a7b-21da560fd47c" />
<img width="2554" height="1440" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/963606ec-6b6a-459d-97ff-80f72e9f5854" />
<img width="2561" height="1440" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/1e1e8275-acc1-4c46-ba79-3eb90e3b2f63" />
