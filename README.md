# Azure-Honeynet-SOC
 
 Currently under construction...

This project showcases a live honeynet/SOC environment hosted within Microsoft Azure using several of its services like Entra ID, Sentinel, and Virtual Machines.
This simulation aims to mimic a corporate environment and the potential attack vectors its network can be prone to.

![screenshot](/Pictures/Overview.jpg)

Here, we have some VM's set up for our "attack" simulation

![screenshot](/Pictures/VM's.png)

We have to configure the Network Security Group for each VM. 

![screenshot](/Pictures/NSG's.png)

Let's just take a look at the Windows one. We implemented a rule where all of the ports are open, so that hackers are more enticed to exploit it.

![screenshot](/Pictures/NSG-win.png)