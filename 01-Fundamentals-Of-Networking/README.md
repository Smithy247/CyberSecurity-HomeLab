
# Fundamentals of Networking

##Objective
Set up two VMs on the same isolated network in Oracle VirtualBox to test the connectivity between them and confirm they can communicate.

##Lab Setup
Tools/Software used:
-Oracle VirtualBox
-Linux Mint (installed on both VMs)

Virtual Machines:
-VM1: Mintx64 (Test 1)
-VM2: Mintx64 Clone (cloned from VM1)

Networking mode:
-Host-Only Adapter this was chosen because it creates a private, isolated network between the host and VMs (or VM-to-VM), without exposing them to the internet or your home network.

##Steps
1. Clone my VM so that I have two VMS for this project.
2. Go into the settings of my cloned VM, go to network and change its mac address so that it is not the same as the original VM.
3. I then opened the terminal on both VMS and typed the command IP a to confirm what both IP addresses are and to make sure they are not the same.
4. Next run the ping command with the other VMS IP address, for example (ping 192.168.56.101).
5. Confirmed successful communication between the two VMs, shown by continuous replies and 0% packet loss, then stopped the ping using Ctrl + C.

##Commands Used
-ip a
-ping 192.168.56.101
-ping 192.168.56.102

##Results
<img width="910" height="896" alt="image" src="https://github.com/user-attachments/assets/b13f9e71-3e1e-4e1f-807c-21785642d788" />

<img width="772" height="810" alt="image" src="https://github.com/user-attachments/assets/f1ca0ab3-13ed-4159-9b30-24f54100c429" />



##Key Concepts

##Challenges/Issues
When I cloned my VM, I ran ip a on both machines to check their network info and noticed something odd — the MAC address and IP address were exactly the same on both. VirtualBox copies the network config when you clone a VM, so both machines were showing up as the same device on the network, which meant they couldn't actually talk to each other properly and when I ran the ping command it would just appear to be talking to itself and not the other VM.

To fix this, I went into the cloned VM's settings and generated a new MAC address, then restarted it. After that, it picked a new IP different from the original, and everything worked as expected, I could ping between the two VMs with 0% packet loss.

lesson learned: when cloning VMs for a lab like this, always double check the network settings afterward rather than assuming it's ready to go.

##Skills Demonstrated

##
