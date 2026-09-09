# Fundamentals of Networking

##Objective

##Lab Setup

<img width="1279" height="888" alt="image" src="https://github.com/user-attachments/assets/a57f7e16-226a-4caa-a481-f95fac1819a7" />


##Steps

##Commands Used

##Results

##Key Concepts

##Challenges/Issues
When I cloned my VM, I ran ip a on both machines to check their network info and noticed something odd — the MAC address and IP address were exactly the same on both. VirtualBox copies the network config when you clone a VM, so both machines were showing up as the same device on the network, which meant they couldn't actually talk to each other properly and when I ran the ping command it would just appear to be talking to itself and not the other VM.

To fix this, I went into the cloned VM's settings and generated a new MAC address, then restarted it. After that, it picked a new IP different from the original, and everything worked as expected, I could ping between the two VMs with 0% packet loss.

lesson learned: when cloning VMs for a lab like this, always double check the network settings afterward rather than assuming it's ready to go.

##Skills Demonstrated

##
