Active Directory Home Lab – Verification and Testing Steps


Prepared by: Jeremy Banks

Environment: Active Directory Home Lab

1. Purpose


This document outlines the verification and testing steps performed to confirm that the Active Directory home lab environment is fully functional, including network connectivity, DNS resolution, and domain authentication, given that the domain controller is running DHCP and the client server has a static IP address.

2. Environment Overview
Domain Controller (DC): Windows Server 2019/2022

Roles: Active Directory Domain Services (AD DS), DNS

Network Configuration: DHCP enabled

Client Server: Windows 10/11

Domain Membership: lab.local

Network Configuration: Static IP assigned manually

DNS Server: Points to the DC

3. Verification and Testing Steps
Network Connectivity

Used ping to verify connectivity between the client server and the DC.

Confirmed consistent response times without packet loss.

IP Configuration Verification

Ran ipconfig /all on both DC and client server.

Verified that the DC receives an IP dynamically via DHCP.

Confirmed the client server has a static IP within the same subnet as the DC and that its DNS is set to the DC’s IP address.

DNS Resolution

Executed nslookup lab.local on the client server.

Confirmed the domain name resolved correctly to the DC’s IP.

Domain Authentication

Logged into the client server using a domain account.

Confirmed successful authentication and access to domain resources.

Active Directory Verification

Opened Active Directory Users and Computers (ADUC) on the DC.

Verified that client objects are visible and that changes (creating or modifying users/groups) are reflected properly.

Service Verification

Confirmed that DNS and Active Directory Domain Services are running on the DC via services.msc.

Ensured no service errors were present.

4. Outcome
Network connectivity between client and DC is verified.

DNS resolution and domain authentication are functioning correctly.

The lab demonstrates proper Active Directory operation even with the DC using DHCP and the client server on a static IP.

The environment is stable and ready for testing, demonstration, or further lab exercises.
