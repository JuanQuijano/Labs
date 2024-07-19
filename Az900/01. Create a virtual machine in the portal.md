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

### Task 2: Connect to the virtual machine ###
In this task, we will connect to our new virtual machine using RDP (Remote Desktop Protocol).

1. Click on bell icon from the upper blue toolbar, and select 'Go to resource' when your deployment has succeded.
Note: You could also use the Go to resource link on the deployment page

2. On the Overview blade, select the Connect dropdown and then select Connect.
Note: The following directions tell you how to connect to your VM from a Windows computer. On a Mac, you need an RDP client such as this Remote Desktop Client from the Mac App Store and on a Linux computer you can use an open source RDP client.

3. On the myVM | Connect page, keep the default options to connect with the public IP address over port 3389 and click Download RDP File under Native RDP. A file will download on the top right of your screen. If you get a warning message, select Keep from the top right of the screen.

4. Open the downloaded RDP file (located on the top right of the browser) by selecting Open file and click Connect when prompted.

5. In the Windows Security window, sign in using the Admin Credentials you used when creating your VM Administrador and the password Pa55w0rd1234! and then click OK.

You may receive a warning certificate during the sign-in process. Click Yes or to create the connection and connect to your deployed VM. You should connect successfully.

A new Virtual Machine (myVM) will launch inside your Lab. Close the Server Manager and dashboard windows that pop up (click "x" at top right). You should see the blue background of your virtual machine. 

<b>Congratulations! You have deployed and connected to a Virtual Machine running Windows Server.</b>
