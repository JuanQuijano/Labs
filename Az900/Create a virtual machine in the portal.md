# Create a virtual machine in the portal #

## Module 01: Create a virtual machine in the portal ##

### Task 1: Create the virtual machine ###

1. On the Windows taskbar, click Microsoft Edge icon to open it. Copy and paste the link https://portal.azure.comand then press Enter to open the Azure portal.

2. On the above searchbar search for and select Virtual machines, and then click +Create and choose Azure Virtual machine from the drop down.

3. On the Basics tab, fill in the following information (leave the defaults for everything else):
* Subscription: Use default supplied
* Resource group: Use default supplied
* Virtual machine name: myVM
* Region: default
* Availability options: No infrastructure redundancy options required
* Security Type: Standard
* Image: Windows Server 2022 Datacenter: Azure Edition - x64 Gen2
* Size: Standard DS1_v2
* Username: Administrador
* Password: Pa55w0rd1234!
* Inbound port rules: Allow select ports
  * Select inbound ports: RDP (3389) and HTTP (80)
* Licensing: Check both
* Select Next: Disks > then select Next: Networking > to switch to the Networking tab to ensure HTTP (80) and RDP (3389) are selected in section Public inbound ports.
* Select Next: Management and then select Next: Monitoring > to switch to the Monitoring section, select the following setting:
  * Boot diagnostics: Disable
* Leave the remaining values on the defaults and then click the Review + create button at the bottom of the page.

Once Validation is passed click the Create button. It can take anywhere from five to seven minutes to deploy the virtual machine.

You will receive updates on the deployment page and via the Notifications area (the bell icon in the top menu bar).
