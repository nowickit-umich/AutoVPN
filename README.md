# Auto VPN
Auto VPN is an open-source solution designed to eliminate reliance on expensive and untrustworthy VPN providers. It enables users to deploy a secure, high-performance VPN server on any cloud service provider with minimal effort, and connect via a user-friendly client application.

Global Deployment: Spin up a VPN server in any geographic region supported by your chosen cloud provider, giving you complete control over location and latency.

DNS Filtering: Built-in DNS filtering on the server blocks ads, trackers, and malicious domains to enhance privacy and security.

Cost-Effective: Operates at approximately $0.0052/hour, or $0.31/month for 15 hours of usage per week.

<img width="242" alt="vpncosts" src="https://github.com/user-attachments/assets/5b3de0e6-48ea-4c89-b9f3-0e5c69640b2c" />

Usage-Based Billing: Pay only for the time you actively use the VPN.

Performance: Optimized for a 25 Mbps connection—sufficient for 4K video streaming.

# Demo
This video demonstrates a new VPN server being created, DNS filtering to perform AD blocking.

https://youtu.be/zxo3843Qp0E

# Components
There are two main components of this project: the VPN client and the VPN server.

VPN Client:
Developed in Python using the cross-platform Kivy framework, the client provides a streamlined interface for starting servers and managing VPN connections.

VPN Server: 
Deployed on Ubuntu and powered by strongSwan, a robust and widely adopted IPsec-based VPN solution. The server is configured automatically for performance, security, and availability.

# Client Architecture Overview
![AutoVPN_ArchOverview](https://github.com/user-attachments/assets/e58ddcbe-d330-4505-b9a0-9dd65d91cd8c)



# AWS Cloud Key Instructions
Creating Access/Secret Key

Log into AWS
1. Go to IAM (Identity and Access Management) Dashboard
2. Go to users tab on the left side of the screen, found between User Groups and Roles options under Access Management
3. Create a new user
4. Set the permissions as "Attach Policies Directly", giving it one policy of AmazonEC2FullAccess, ignore permission boundaries. (More limited policies can be used if greater security is desired)
5. Review and create the user
6. Click on the user and press create access key on the right side of the summary box
7. For Access key best practices & alternatives, select "Application running outside AWS"
8. Add description tag (not required)
9. The keys are now created, save them in a secure location, these will be used to log into the VPN program
10. The secret key can not be seen again after exiting the tab

Do not put the keys in a public spot or in code, as other people who have access to the key can use it to create servers


NOTE: 
Initially developed as a university software engineering project: https://github.com/nowickit-umich/CIS375GroupProject
