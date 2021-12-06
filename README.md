In the project, you are able to develop and program DevOps product. Your application, program or web service must detect and report about network/device changes, during this task you learn about different technologies and features than you need to build a **monitoring system**.


In this work you will use both the Southbound APIs (CLI, SNMP ...) and the Northbound APIs (Web UI, RESTful). This cooperation will allow you to learn how to interact with the network from different parties. Also you can improve your teamwork skills.


**Network programmability** is a set of tools to deploy, manage, and troubleshoot a network device. A programmability-enabled network is driven by intelligent software that can deal with a single node or a group of nodes or even or address the network with a single unifying element. The toolchain uses application programming interfaces or APIs, which serve as the interface to the device or controller. The toolchain also utilizes software that uses the API to gather data or intelligently build configurations.

![Network programmability](https://raw.githubusercontent.com/oborys/np1/master/network_programmability.png)

- [CLI guide: Cisco Catalyst 9300 Series Switches](https://www.cisco.com/c/en/us/td/docs/switches/lan/catalyst3850/software/release/3se/consolidated_guide/command_reference/b_consolidated_3850_3se_cr.pdf) 
- [CLI guide Cat 9000](https://www.cisco.com/c/en/us/td/docs/switches/lan/catalyst9300/software/release/16-5/command_reference/b_165_9300_cr.pdf)

Link to a video review of some work:

- https://www.youtube.com/watch?v=1eZmoon0-pM

For testing some additional features you are able to book sandbox with some equipment.

In the instructions below you can see how to work with DNA-C hardware sandbox. 

Pre-launch settings:
Download and install next items:
* [Download the Cisco AnyConnect VPN Client software.](https://developer.cisco.com/site/sandbox/anyconnect/) or install with Managed Software Center.
* [Installation Guide for Cisco AnyConnect VPN Client software.](https://devnetsandbox.cisco.com/Docs/VPN_Access/AnyConnect_Installation_Guide.pdf)


1 Reserve the selected lab on the site
https://devnetsandbox.cisco.com/RM/Topology
You can reserved next labs:
* DNA-C Labs 1 & 2: These labs contain a Virtual DNA-C system, a Linux DevBox, and a sample topology of real hardware.
* DNA-C Labs 3 & 4: These labs contain a Hardware DNA-C Appliance, a Linux DevBox, and a sample topology of real hardware.
![Reserve lab](https://raw.githubusercontent.com/oborys/np1/master/sandbox_dna-c_new.png) 

If there is now available lab for this moment you can schedule reservation, and chose time from available slots (push “Reserve” button for this, time zone - GMT, local Kyiv time GMT time from gui plus 3h)
![available slots](https://raw.githubusercontent.com/oborys/np1/master/available_slots_dna-c.png) 

2 After the 30-minute setup, you will receive an email with credentials

3 Connect according to this guide https://devnetsandbox.cisco.com/Docs/VPN_Access/AnyConnect_Connection_Guide.pdf 


4 To access the DNA-C web interface, you must copy the IP address from the interfaces of the lab and paste it into the browser.
![DNA-C web interface](https://raw.githubusercontent.com/oborys/np1/master/http_access_dna.png)  

Login and password for each lab on the left in the description, IP address - in the topology under the inscription DNA-Center Controller ...

5 Sometimes, when credentials do not receive on email, they can be seen in the interface of the booked infrastructure by clicking on the "OUTPUT"
![DNA-C web interface](https://raw.githubusercontent.com/oborys/np1/master/output_dna-c_1.png)

If you close tab with lab settings, you can reopen it by clicking reservations https://devnetsandbox.cisco.com/RM/Reservation/List 
![reservations](https://raw.githubusercontent.com/oborys/np1/master/reservations_dna-c.png)


6 After open DNA-C GUI Interface in the browser go to Topology to discover inventory. Click “Discovery”
![DNA-C GUI Interface](https://raw.githubusercontent.com/oborys/np1/master/inventory_dna-c.png)

Also, you can go to each device directly using ssh.
All credentials you can see by clicking Lab Topology Diagram
![Lab Topology Diagram](https://raw.githubusercontent.com/oborys/np1/master/go_to_lab_topology_diagram.png)

Lab devices credentials (for example)
![Lab Topology Diagram](https://raw.githubusercontent.com/oborys/np1/master/ssh_credentials_dna-c.png)

In choose range and add, for example for lab above I add
10.10.20.80 - 10.10.20.85 and push “+”
- DNA-Center Controller:
	- IP: 10.10.20.85
	- SSH: (Port 2222) with credentials [maglev/Grapevine1]
	- HTTP: with credentials [admin/Cisco1234!]

**Credentials**

**CLI**: 
* login: admin
* password: ciscopsdt

**SNMP**:
* name/description: rw
* write community: cisco123


Success discovering of inventory
![Success discovering of inventory](https://raw.githubusercontent.com/oborys/np1/master/discovery_dna-c.png)
 
Also you need to enable API Bundles.
In main page you need go to Platform EFT
OR you can see rest api documentation here https://developer.cisco.com/site/dna-center-rest-api/ 
![Platform EFT](https://raw.githubusercontent.com/oborys/np1/master/platform_api_bundles_dna-c.png)
