VPN Lab: Testing VPN Behavior with Azure VM and ProtonVPN

Overview

This lab demonstrates how VPN usage can alter public IP addresses and influence regional web content. A Windows 10 virtual machine was deployed in Azure, connected to ProtonVPN, and tested for geolocation-based changes in web browsing.

1. Initial IP Address Logging

Started by recording the public IP address of the local machine:

- Navigated to [https://whatismyipaddress.com/](https://whatismyipaddress.com/)
- Saved the displayed IP for reference later in the lab

2. Azure Virtual Machine Deployment

Provisioned a Windows 10 virtual machine in Azure, selecting a geographic region outside of the local area:

- Created a new **Resource Group**
- Deployed the VM in a different country
- Connected via Remote Desktop (RDP)

Once inside the VM:

- Visited [https://whatismyipaddress.com/](https://whatismyipaddress.com/) to capture the VM’s public IP
- Logged this second IP address to compare against later VPN testing

3. ProtonVPN Installation and VPN Testing

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
