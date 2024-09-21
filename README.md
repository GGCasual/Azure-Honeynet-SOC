# Azure-Honeynet-SOC
 
 <h3><i>Currently under construction...</i></h3>

This project showcases a live honeynet/SOC environment hosted within Microsoft Azure using several services like Entra ID, Sentinel, and Virtual Machines.
This simulation aims to mimic a corporate network environment and the potential attack vectors it can be prone to.

![screenshot](/Pictures/Overview.png)

Topology of our Lab:
![screenshot](/Pictures/Lab-VNet.png)

Here, we have some VM's set up for our "attack" simulation.

![screenshot](/Pictures/VM's.png)

We have to configure the Network Security Group for each VM. 

![screenshot](/Pictures/NSG's.png)

Let's take a look at the Windows one. Here, we would implement an inbound security rule named "DANGER_AllowAnyCustomAnyInbound," where all the ports are left open so that hackers are more enticed to exploit it.

![screenshot](/Pictures/NSG-win.png)


Here, we brute force some login attempts to our Windows-VM and filtered out the Security Event logs from it. We then queried the logs to filter specific information about our "attack" attempts. Based on the KQL query that we constructed, important information like my device's IP address and geographic coordinates are now shown.

![screenshot](/Pictures/KQL-Log-Query.png)


This is a more visual representation of our logs from the vulnerable VM's:

![screenshot](/Pictures/Updated%20Workbook%20Pics/linux-ssh-auth-fail-BEFORE.png)

![screenshot](/Pictures/Updated%20Workbook%20Pics/windows-rdp-auth-fail-BEFORE.png)

![screenshot](/Pictures/Updated%20Workbook%20Pics/nsg-malicious-allowed-in-BEFORE.png)


We then configure Microsoft Sentinel with custom alerts:

![screenshot](/Pictures/Sentinel-Incidents.png)


Here's some statistics from Event Viewer (windows-vm) and Syslog (linux-vm) after we left our VM's vulnerable to the internet and before we implemented any security measurements:

![screenshot](/Pictures/Updated%20Workbook%20Pics/BEFORE-Map-Stats.png)

And here's the statistics after some security implementation, based on the NIST 800-53 framework:

![screenshot](/Pictures/Updated%20Workbook%20Pics/AFTER-Map-Stats.png)

