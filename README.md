<p align="center">
  <<img width="642" height="351" alt="Logo Screenshot" src="https://github.com/user-attachments/assets/381dabf8-d8a2-4630-a94b-e04705c5a482" />
>
</p>

# VPN Traffic Routing Lab

## 📝 Description
In this lab, I built a cloud-based infrastructure to analyze how network traffic behaves when routed through different geographical locations. By integrating Microsoft Azure with Proton VPN, I simulated real-world scenarios to understand how data travels between a user and a public cloud environment.

## 🛠️ Key Concepts Covered
#VPN Configuration & Tunneling: Gained hands-on experience in setting up secure connections to manage and redirect network traffic.
#Geo-Location Analysis: Observed how changing a connection point affects regional traffic behavior and content delivery.
#Infrastructure Skills: Managed cloud-hosted resources in Azure, building a solid foundation for network administration and security troubleshooting.

---

## 📸 Step-by-Step Lab Walkthrough

### 🔹 Phase 1: Resource Group Setup

Step 1: Local PC IP Check: Recorded my local computer's public IP address to establish for starting the cloud setup
<br>
<<img width="1366" height="768" alt="Screenshot 1 Local PC IP Address" src="https://github.com/user-attachments/assets/03e02a9b-b972-4578-ae3b-2b4becbbce6a" />
>
<br>
<br>

Step 2: Resource Group Setup: Created a "Resource Group dumela" in Azure to act as a container for all the files and tools I would be using in this lab.
<br>
<<img width="1366" height="768" alt="Screenshot 2 Resource Group Creation Azure" src="https://github.com/user-attachments/assets/f9d499b2-b898-4613-bf3d-92a28007e8b7" />
>
<br>
<br>

Step 3: Deployment Verification: Confirmed that the Resource Group was successfully created and ready for use.
<br>
<<img width="1366" height="768" alt="Screenshot 3 Resource Group Created Azure" src="https://github.com/user-attachments/assets/b6688090-2dd1-4d1e-852e-d9c6d372b88d" />
>
<br>

---

### 🔹 Phase 2: Virtual Machine Setup 

Step 4: VM Configuration: Selected the settings for the Virtual Machine (VM), choosing the region and basic performance specs.
<br>
<<img width="1366" height="768" alt="Screenshot 4 Virtual Machine Creation" src="https://github.com/user-attachments/assets/68472c83-e67e-4034-9993-3bb2a6000803" />
>
<br>
<br>

Step 5: OS Selection: Chose the Windows Server 2022 operating system to run on the virtual machine.
<br>
<<img width="1366" height="768" alt="Screenshot 5 Virtual Machine Creation" src="https://github.com/user-attachments/assets/a217b5c6-4868-4896-a97f-0d8db73632d3" />
>
<br>
<br>


Step 6: Firewall/Security: Opened the necessary port (3389) in the firewall to allow me to connect to the machine remotely.
<br>
<<img width="1366" height="768" alt="Screenshot 6 Virtual Machine Creation 8" src="https://github.com/user-attachments/assets/bfa1b311-d005-4612-be54-2d568ffc6af6" />
>
<br>
<br>

Step 7: Validation: Ran a final check in Azure to make sure all my settings were correct before launching.
<br>
<<img width="1366" height="768" alt="Screenshot 7  Virtual Machine Creation" src="https://github.com/user-attachments/assets/1444ee74-41d9-4977-b9ca-6566afaaded2" />
>
<br>
<br>

Step 8: Deploying the VM: Initiated the build process to create the virtual machine, network, and storage.
<br>
<<img width="1366" height="768" alt="Screenshot 8 Virtual Machine Created-Deployed" src="https://github.com/user-attachments/assets/88b646bc-f61f-475e-aca2-db8d3aa9ec27" />
>
<br>

---

### 🔹 Phase 3: Accessing the Virtual Machine

Step 9: Checking Public IP: Verified the public IP address that Azure assigned to my new virtual machine
<br>
<<img width="1366" height="768" alt="Screenshot 9 Virtual Machine IP Address - VPNSyber" src="https://github.com/user-attachments/assets/b5382f58-b2a4-46ec-826d-4b2c5eaf774d" />
>
<br>
<br>

Step 10: Remote Login (RDP): Used Remote Desktop to connect to the Windows Server running in the cloud.
<br>
<<img width="1366" height="768" alt="Screenshot 10 Logging in Virtual Machine - VPN Cyber" src="https://github.com/user-attachments/assets/21900d25-8490-4f1e-9175-4f488d9c8c39" />
>
<br>
<br>

Step 11: Desktop Access: Successfully logged in and accessed the remote Windows desktop environment.
<br>
<<img width="1366" height="768" alt="Screenshot 11 Logged in to Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/ce73dcf8-9775-40c3-bb6d-367392c1e448" />
>
<br>
<br>

Step 12: VM IP Verification: Checked the VM's public IP address again from inside the machine to confirm it was using Azure's network.
<br>
<<img width="1366" height="768" alt="Screenshot 12 Virtual Macchine IP Address VPNSyber IP addresss" src="https://github.com/user-attachments/assets/01b02ef0-cf5c-42bd-847f-61b52946cb86" />
>
<br>

---

### 🔹 Phase 4: VPN & Traffic Routing

Step 13: Download VPN: Downloaded the Proton VPN installer onto the remote virtual machine.
<br>
<<img width="1366" height="768" alt="Screenshot 13 Downloading Proton VPN on Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/97a17d63-a7e3-45f3-8503-94efd67c1046" />
>
<br>
<br>

Step 14: Install VPN: Installed the VPN software on the Windows Server.
<br>
<<img width="1366" height="768" alt="Screenshot 14 Installing Proton VPN on Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/6099c371-017a-4f66-96a7-2625a34a309c" />
>
<br>
<br>

Step 15: Launch VPN: Opened the VPN application to prepare the connection.
<br>
<<img width="1366" height="768" alt="Screenshot 15 Virtual Machine VPNSyber IP on Proton VPN" src="https://github.com/user-attachments/assets/4c0d6f82-68f2-4182-9aa7-bfd180d64863" />
>
<br>
<br>

Step 16: Connect to VPN: Activated the VPN to tunnel the VM’s internet traffic through a secure, third-party server.
<br>
<<img width="1366" height="768" alt="Screenshot 16 Connecting to Proton VPN on Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/2a296c69-80c4-4e81-bc2d-60dc83f30b70" />
>
>
<br>
<br>

Step 17: Verify Location Shift: Checked the IP address inside the VM again to confirm that the location had changed, proving the traffic was successfully routed through the VPN.
<br>
<<img width="1366" height="768" alt="Screenshot 17 Change of IP Address Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/1b92748b-4a5e-4aa4-9fca-ddaf199c918b" />
>
<br>

---

### 🔹 Phase 5: Resource Lifecycle Management & Termination

Step 18: Disconnect: Closed the Remote Desktop session.
<br>
<<img width="1366" height="768" alt="Screenshot 18 Closing Virtual Machine VPNCyber" src="https://github.com/user-attachments/assets/2fc89ef8-d144-4ca9-93b8-1e3ef500c0de" />
>
<br>
<br>

Step 19: Delete VM: Sent the command to delete the virtual machine now that the test was complete.
<br>
<<img width="1366" height="768" alt="Screenshot 19 Deleting Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/964eb16c-14b4-40b8-a2ec-43e15620c477" />
>
<br>
<br>

Step 20: Confirm Deletion: Verified that the virtual machine was removed from the system.
<br>
<<img width="1366" height="768" alt="Screenshot 20 Virtual Machine Deleted" src="https://github.com/user-attachments/assets/c1f98fa1-6687-457a-989c-00ec29ef9add" />
>
<br>
<br>

Step 21: Delete Resource Group: Deleted the main Resource Group container to remove all associated files and network components.
<br>
<<img width="1366" height="768" alt="Screenshot 21 Deleting Resource Group" src="https://github.com/user-attachments/assets/3263bdc4-a231-4327-9bc5-e910157547a2" />
>
<br>
<br>

Step 22: Final Audit: Did a final check to ensure all resources were deleted, ensuring there are no ongoing costs.
<br>
<<img width="1366" height="768" alt="Screenshot 22 Deleted Resource Group" src="https://github.com/user-attachments/assets/c4d9f7ab-82bc-4b6e-8256-95a1769823fa" />
>
<br>

---

## 🏁 Conclusion & Key Takeaways

This lab successfully showed how cloud networks work and how VPNs can reroute traffic.

Understanding IP Locations: I learned how a machine’s public IP is tied to the physical data center, regardless of where I am sitting.

Traffic Routing: By using a VPN, I saw how you can bypass standard network paths and change how websites "see" your location.

Cloud Governance: Most importantly, I practiced "cleaning up" after myself. Managing cloud costs by deleting unused resources is a critical skill for any IT professional.
