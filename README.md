# Azure-Honeynet-SOC
 
 <h1><i>Currently under construction...</i></h1>

This project showcases a live honeynet/SOC environment hosted within Microsoft Azure using several of its services like Entra ID, Sentinel, and Virtual Machines.
This simulation aims to mimic a corporate environment and the potential attack vectors its network can be prone to.

![screenshot](/Pictures/Overview.png)

Here, we have some VM's set up for our "attack" simulation.

![screenshot](/Pictures/VM's.png)

We have to configure the Network Security Group for each VM. 

![screenshot](/Pictures/NSG's.png)

Let's take a look at the Windows one. Here, we would implement an inbound security rule named "DANGER_AllowAnyCustomAnyInbound," where all the ports are left open so that hackers are more enticed to exploit it.

![screenshot](/Pictures/NSG-win.png)