Create a Simple Network With Cisco Packet Tracer



![Screenshot 2023-07-05 130042](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/14f854c5-6676-4295-a450-dec03710349a)


Objectives 

Part 1: Build a simple network in the logical topology workspace

Part 2: Configure the Network Devices

Part 3: Test Connectivity between Network Devices

Part 4: Save the file and close the packet tracer



Part 1: Build a Simple Network in the Logical Topology Workspace

Step 1: Launch Packet Tracer.

a. Launch Packet Tracer on your PC or laptop computer

Double-click on the Packet Tracer icon on your desktop or navigate to the directory that contains the
Packet Tracer executable file and launch Packet Tracer. Packet Tracer should open with a blank default
Logical topology workspace as shown in the figure.

![image](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/2cf2a9d7-8ddf-4671-a55e-dab4b3731b05)



Step 2: Build the topology

a. Add network devices to the workspace

Using the device selection box, add the network devices to the workspace as shown in the topology
diagram.
To place a device onto the workspace, first choose a device type from the Device-Type Selection box.
Then, click on the desired device model from the Device-Specific Selection box. Finally, click on a
location in the workspace to put your device in that location. If you want to cancel your selection, click the
Cancel icon for that device. Alternatively, you can click and drag a device from the Device-Specific
Selection box onto the workspace.


b. Add network devices to the workspace.

Using the device selection box, add the network devices to the workspace as shown in the topology
diagram
To place a device onto the workspace, first choose a device type from the Device-Type Selection box.
Then, click on the desired device model from the Device-Specific Selection box. Finally, click on a
location in the workspace to put your device in that location. If you want to cancel your selection, click the
Cancel icon for that device. Alternatively, you can click and drag a device from the Device-Specific
Selection box onto the workspace.

c. Change display names of the nework devices.

To change the display names of the network devices click on the device icon on the Packet Tracer
Logical workspace, then click on the Config tab in the device configuration window. Type the new name
of the device into the Display Name box as show in the figure below

 ![Screenshot 2023-07-05 130934](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/27fc65e6-e0c4-41ab-b144-c11c36a527ab)

d. Add the physical cabling between devices on the workspace

Using the device selection box, add the physical cabling between devices on the workspace as shown in
the topology diagram.
The PC will need a copper straight-through cable to connect to the wireless router. Select the copper
straight-through cable in the deviceselection box and attach it to the FastEthernet0 interface of the PC
and the Ethernet 1 interface of the wireless router.

The wireless router will need a copper straight-through cable to connect to the cable modem. Select the
copper straight-through cable in the device-selection box and attach it to the Internet interface of the
wireless router and the Port 1 interface of the cable modem.
The cable modem will need a coaxial cable to connect to the Internet cloud. Select the coaxial cable in
the device-selection box and attach it to the Port 0 interface of the cable modem and the coaxial interface
of the Internet cloud.
The Interne cloud will need copper straight-through cable to connect to the Cisco.com server. Select the
copper straight-through cable in the device-selection box and attach it to the Ethernet interface of the
Internet cloud and the FastEthernet0 interface of the Cisco.com server.

 

Part 2: Configure the Network Devices

Step 1: Configure the wireless router

a. Create the wireless network on the wireless router
Click on the Wireless Router icon on the Packet Tracer Logical workspace to open the device
configuration window.
In the wireless router configuration window, click on the GUI tab to view configuration options for the
wireless router.
Next, click on the Wireless tab in the GUI to view the wireless settings. The only setting that needs to be
changed from the defaults is the Network Name (SSID). Here, type the name “HomeNetwork” as shown
in the figure.



![Screenshot 2023-07-05 131233](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/12ffdbbf-165b-49b0-aa85-aa43c36fdbc3)


In the DHCP Server settings verify that the Enabled button is selected and configure the static IP
address of the DNS server as 208.67.220.220 as shown in the figure.

![Screenshot 2023-07-05 131410](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/806e2b53-a43b-4c94-80bb-883fd910e180)



Step 2: Configure the laptop

a. Configure the Laptop to access the wireless network
Click on the Laptop icon on the Packet Tracer Logical workspace and in the laptop configuration
windows select the Physical tab.
In the Physical tab you will need to remove the Ethernet copper module and replace it with the Wireless
WPC300N module.
To do this, you first power the Laptop off by clicking the power button on the side of the laptop. Then
remove the currently installed Ethernet copper module by clicking on the module on the side of the laptop
and dragging it to the MODULES pane on the left of the laptop window. Then install the Wireless
WPC300N module by clicking on it in the MODULES pane and dragging it to the empty module port on
the side of the laptop. Power the laptop back on by clicking on the Laptop power button again.


With the wireless module installed, the next task is to connect the laptop to the wireless network.
Click on the Desktop tab at the top of the Laptop configuration window and select the PC Wireless icon.
Once the Wireless-N Notebook Adapter settings are visible, select the Connect tab. The wireless network
“HomeNetwork” should be visible in the list of wireless networks as shown in the figure.
Select the network, and click on the Connect tab found below the Site Information pane.


![Screenshot 2023-07-05 131851](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/e690fd6b-5a85-4e18-825e-1e8165742340)



Step 3: Configure the PC

a. Configure the PC for the wired network
Click on the PC icon on the Packet Tracer Logical workspace and select the Desktop tab and then the
IP Configuration icon.
In the IP Configuration window, select the DCHP radio button as shown in the figure so that the PC will
use DCHP to receive an IPv4 address from the wireless router. Close the IP Configuration window.


![Screenshot 2023-07-05 133310](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/4f5b7970-26f2-4e00-9e9a-3df927154993)


Click on the Command Prompt icon. Verify that the PC has received an IPv4 address by issuing the
ipconfig /all command from the command prompt as shown in the figure. The PC should receive an IPv4
address in the 192.168.0.x range.

![Screenshot 2023-07-05 133338](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/bbbc4071-2c72-4196-a226-b41ec7cd44bb)


Step 4: Configure the Internet cloud

a. Install network modules if necessary
Click on the Internet Cloud icon on the Packet Tracer Logical workspace and then click on the Physical
tab. The cloud device will need two modules if they are not already installed. The PT-CLOUD-NM-1CX
which is for the cable modem service connection and the PT-CLOUD-NM-1CFE which is for a copper
Ethernet cable connection. If these modules are missing, power off the physical cloud devices by clicking
on the power button and drag each module to an empty module port on the device and then power the
device back on.

b. Identify the From and To Ports
Click on the Config tab in the Cloud device window. In the left pane click on Cable under
CONNECTIONS. In the first drop down box choose Coaxial and in the second drop down box choose
Ethernet then click the Add button to add these as the From Port and To Port as shown in the figure.




![Screenshot 2023-07-05 133547](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/a0bdefdb-e6a4-44ed-a752-3bf88a3e6948)


Identify the type of provider
While still in the Config tab click Ethernet under INTERFACE in the left pane. In the Ethernet
configuration window select Cable as the Provider Network as shown in the figure




![Screenshot 2023-07-05 133850](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/3bcb490c-a4a1-4ae4-b95c-73c587e9ab7f)



Step 5: Configure the Cisco.com server
a. Configure the Cisco.com server as a DHCP server
Click on the Cisco.com server icon on the Packet Tracer Logical workspace and select the Services tab.
Select DHCP from the SERVICES list in the left pane.

In the DHCP configuration window, configure a DHCP as shown in the figure with the following settings.
  Click On to turn the DCHP service on
  Pool name: DHCPpool
  Default Gateway: 208.67.220.220
  DNS Server: 208.67.220.220
  Starting IP Address: 208.67.220.1
  Subnet Mask 255.255.255.0
  Maximum number of Users: 50
  
Click Add to add the pool

![Screenshot 2023-07-05 134415](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/05504a58-0ef1-4e71-a9c6-b4c36b6de15a)


b. Configure the Cisco.com server as a DNS server to provide domain name to IPv4 address resolution.
While still in the Services tab, select DNS from the SERVICES listed in the left pane.
Configure the DNS service using the following settings as shown in the figure.

  Click On to turn the DNS service on
  
  Name: Cisco.com
  
  Type: A Record
  
  Address: 208.67.220.220

Click Add to add the DNS service settings

![Screenshot 2023-07-05 134511](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/215c2dea-1b64-4fc7-a9ad-1c5697ffb818)


c. Configure the Cisco.com server Global settings.
Select the Config tab.

Click on Settings in left pane.

Configure the Global settings of the server as follows:

 Select Static
 
 Gateway: 208.67.220.1
 
 DNS Server: 208.67.220.220

 
![Screenshot 2023-07-05 134551](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/493890c8-24d9-487a-882d-72381a6ff8f5)



d. Configure the Cisco.com server FastEthernet0 Interface settings.
Click on FastEthernet in left pane of the Config tab
Configure the FastEthernet Interface settings of the server as follows:

Select Static under IP Configuration

IP Address: 208.67.220.220

Subnet Mask: 255.255.255.0

![Screenshot 2023-07-05 134648](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/5319e0db-7271-4ac4-8cbf-2baf234114ab)






Part 3: Verify Connectivity

Step 1: Refresh the IPv4 settings on the PC

a) Verify that the PC is receiving IPv4 configuration information from DHCP.
Click on the PC on the Packet Tracer Logical workspace and then the select the Desktop tab of the PC
configuration window.
Click on the Command Prompt icon

In the command prompt refresh the IP settings by issuing the commands ipconfig /release and then
ipconfig /renew. The output should show that the PC has an IP address in the 192.168.0.x range, a
subnet mask, a default gateway, and DNS server address as shown in the figure




![Screenshot 2023-07-05 134743](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/a2709271-c910-41c0-b3bd-8b9493444ba5)




b) Test connectivity to the Cisco.com server from the PC
From the command prompt, issue the command ping Cisco.com. It may take a few seconds for the ping
to return. Four replies should be received as shown in the figure.



![Screenshot 2023-07-05 134820](https://github.com/MahmutCanGonul/Simple-Network/assets/75094927/055eb643-9176-4973-a73e-3b3e87f4bd80)



Done your server is ready!!!




