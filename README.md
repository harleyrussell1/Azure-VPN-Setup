# VPN Lab: Testing VPN Behavior with Azure VM and ProtonVPN

## Overview

This lab demonstrates how VPN usage can alter public IP addresses and influence regional web content. A Windows 10 virtual machine was deployed in Azure, connected to ProtonVPN, and tested for geolocation-based changes in web browsing.

## Technologies Used

- Microsoft Azure (Resource Groups, Virtual Machines)
- Windows 10 Virtual Machine
- Remote Desktop Protocol (RDP)
- ProtonVPN (client and service)
- IP Geolocation Verification (whatismyipaddress.com)
- Web Proxy & Regional Behavior Testing (Google, Amazon, etc.)

---

## 1. Initial IP Address Logging

Started by recording the public IP address of the local machine:

- Navigated to [https://whatismyipaddress.com/](https://whatismyipaddress.com/)
- Saved the displayed IP for reference later in the lab

---

## 2. Azure Virtual Machine Deployment

Provisioned a Windows 10 virtual machine in Azure, selecting a geographic region outside of the local area:

- Created a new **Resource Group**
- Deployed the VM in a different country
- Connected via Remote Desktop (RDP)

Once inside the VM:

- Visited [https://whatismyipaddress.com/](https://whatismyipaddress.com/) to capture the VM’s public IP
- Logged this second IP address to compare against later VPN testing

---

## 3. ProtonVPN Installation and VPN Testing

Signed up for a free ProtonVPN account using the official website:

- [https://account.protonvpn.com/signup?plan=free](https://account.protonvpn.com/signup?plan=free)

Within the Azure VM:

- Downloaded and installed the ProtonVPN client
- Logged in to [https://account.protonvpn.com/login](https://account.protonvpn.com/login)
- Connected to a VPN server based in **Japan**

After establishing the VPN connection:

- Returned to [https://whatismyipaddress.com/](https://whatismyipaddress.com/) to note the third, VPN-assigned IP address

To observe how location affects web content, several sites were tested:

- [https://www.google.com](https://www.google.com)
- [https://www.amazon.com](https://www.amazon.com)
- [https://www.disney.com](https://www.disney.com)

Regional differences were noted in areas such as language, localized product offerings, and automatic domain redirection.

---

## Skills and Experience Gained

This lab provides practical insight into how VPNs affect network behavior and user experience. Key takeaways include:

- Understanding how **public IP addresses** change across different network contexts: local device, Azure VM, and VPN  
- Using **IP geolocation tools** to verify location changes and confirm VPN effectiveness  
- Installing and configuring a VPN client (ProtonVPN) within a virtualized Windows environment  
- Observing the impact of regional IP addresses on **web content localization**, such as search results, default languages, and regional product availability  
- Using **Remote Desktop Protocol (RDP)** to access and manage remote infrastructure securely  

These skills are essential for professionals working in IT, cybersecurity, and cloud networking, especially in roles involving privacy, geolocation, or remote access solutions.

## Screenshots

All screenshots for this lab can be found in the [screenshots](./screenshots) folder.
