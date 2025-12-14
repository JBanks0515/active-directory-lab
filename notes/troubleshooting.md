DNS and IP Addressing Troubleshooting Report


Prepared by: 
Jeremy Banks


Environment: Active Directory Home Lab
1. Executive Summary


This report documents a DNS and IP addressing issue encountered during the configuration of my Active Directory home lab. The issue was traced to improper static IP configuration on the domain controller, which resulted in DNS resolution failures. Correcting the IP addressing ensured stable domain functionality and reliable name resolution.


2. Environment Overview


Domain Controller

Operating System: Windows Server (2019/2022)

Roles: Active Directory Domain Services, DNS

IP Configuration: Static (Required)



Client System

Operating System: Windows 10/11

Domain Member


3. Issue Description


The Active Directory environment experienced intermittent DNS resolution and connectivity issues. Client systems were unable to consistently locate the domain controller, impacting authentication and access to domain services.


4. Symptoms
Inconsistent domain connectivity

DNS resolution failures

Active Directory services responding unpredictably

Domain controller IP address changing unexpectedly


5. Troubleshooting Methodology


A structured troubleshooting approach was used:

Verified network connectivity between client and domain controller

Reviewed IP configuration using ipconfig /all

Validated DNS server settings

Examined DHCP and network adapter configuration on the domain controller

Reconfirmed whether the domain controller was configured with a static IP address


6. Root Cause Analysis


The domain controller was not consistently configured with a static IP address and was able to receive an address from DHCP. This caused IP changes that disrupted DNS records and Active Directory name resolution.


7. Resolution
Reconfigured the domain controller’s network adapter to use a fixed static IP address

Verified subnet mask, default gateway, and DNS settings

Ensured DHCP was disabled for the domain controller’s adapter

Restarted networking and DNS services to apply changes


8. Outcome
Domain controller maintained a consistent IP address

DNS resolution stabilized

Client systems successfully resolved and authenticated to the domain

Active Directory services operated reliably


9. Key Takeaways
Active Directory domain controllers must always use static IP addressing

DNS stability is directly dependent on consistent IP configuration

Proper network configuration is critical to domain reliability


10. Conclusion


This troubleshooting exercise reinforced best practices for Active Directory infrastructure, specifically the critical role of static IP addressing in DNS and domain stability. The issue was successfully resolved, restoring full functionality to the lab environment.

