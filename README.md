<p align="center">
  <<img width="642" height="351" alt="Logo Screenshot" src="https://github.com/user-attachments/assets/381dabf8-d8a2-4630-a94b-e04705c5a482" />
>
</p>

# 🌐 Public Cloud & VPN Traffic Routing Lab

## 📝 Description
A practical hands-on lab demonstrating cloud virtualization, geographic IP allocation, and encrypted traffic tunneling using Microsoft Azure and ProtonVPN. 

The project involves deploying a Windows Server virtual machine in a remote Azure region, analyzing how public IP addresses change relative to the hosting infrastructure, and subsequently establishing a secure VPN tunnel from within the VM to a third geographic location. This lab highlights the real-world behavior of regional content delivery networks (CDNs), localized web traffic, and geo-spoofing detection mechanisms across platforms like Google and Amazon.

## 🛠️ Key Concepts Covered
* **Cloud Infrastructure:** Provisioning and managing ephemeral compute resources using Azure Resource Groups.
* **Remote Management:** Establishing secure administrative sessions via Remote Desktop Protocol (RDP).
* **Network Virtualization:** Analyzing public-facing IPv4 structures and tracking geographic routing shifts.
* **VPN Tunneling:** Managing protocol-based traffic encapsulation to bypass geographic network restrictions.

---

## 📸 Step-by-Step Lab Walkthrough & Evidence

### 🔹 Phase 1: Environment Baseline & Resource Group Setup

**Step 1: Local PC IP Baseline**
* Documented the public IPv4 address of the local host machine using *whatismyipaddress.com* to establish a clear networking baseline before initializing cloud traffic.
<br>
<<img width="1366" height="768" alt="Screenshot 1 Local PC IP Address" src="https://github.com/user-attachments/assets/03e02a9b-b972-4578-ae3b-2b4becbbce6a" />
>
<br>
<br>

**Step 2: Resource Group Initialization**
* Configuring the foundational logical container (`dumela`) within the Azure Portal UI to aggregate all upcoming lab dependencies.
<br>
<<img width="1366" height="768" alt="Screenshot 2 Resource Group Creation Azure" src="https://github.com/user-attachments/assets/f9d499b2-b898-4613-bf3d-92a28007e8b7" />
>
<br>
<br>

**Step 3: Deployment Verification**
* Confirmed successful orchestration and deployment of the target Resource Group across the Azure control plane.
<br>
<<img width="1366" height="768" alt="Screenshot 3 Resource Group Created Azure" src="https://github.com/user-attachments/assets/b6688090-2dd1-4d1e-852e-d9c6d372b88d" />
>
<br>

---

### 🔹 Phase 2: Virtual Machine Configuration & Provisioning

**Step 4: VM Core Configurations**
* Setting up the compute instance details (`VPNSD06`), region allocation, and setting the redundancy baseline.
<br>
<<img width="1366" height="768" alt="Screenshot 4 Virtual Machine Creation" src="https://github.com/user-attachments/assets/68472c83-e67e-4034-9993-3bb2a6000803" />
>
<br>
<br>

**Step 5: OS Image Selection**
* Navigating the marketplace tier to explicitly choose a Windows Server 2022 image featuring the Desktop Experience GUI environment.
<br>
<<img width="1366" height="768" alt="Screenshot 5 Virtual Machine Creation" src="https://github.com/user-attachments/assets/a217b5c6-4868-4896-a97f-0d8db73632d3" />
>
<br>
<br>

**Step 6: Security & Inbound Port Rules**
* Adjusting firewall controls to explicitly permit inbound traffic via port 3389 to allow Remote Desktop (RDP) sessions.
<br>
<<img width="1366" height="768" alt="Screenshot 6 Virtual Machine Creation 8" src="https://github.com/user-attachments/assets/bfa1b311-d005-4612-be54-2d568ffc6af6" />
>
<br>
<br>

**Step 7: Final Review Validation**
* Running the deployment validation pass within the Azure portal UI to ensure configuration schemas are valid.
<br>
<<img width="1366" height="768" alt="Screenshot 7  Virtual Machine Creation" src="https://github.com/user-attachments/assets/1444ee74-41d9-4977-b9ca-6566afaaded2" />
>
<br>
<br>

**Step 8: Resource Provisioning Live Run**
* Initiating the actual build pipeline, monitoring virtual networking, public IP creation, and storage attachment.
<br>
<<img width="1366" height="768" alt="Screenshot 8 Virtual Machine Created-Deployed" src="https://github.com/user-attachments/assets/88b646bc-f61f-475e-aca2-db8d3aa9ec27" />
>
<br>

---

### 🔹 Phase 3: Cloud Instance Access & Initial Verification

**Step 9: Public IP Assignment Check**
* Reviewing the newly allocated public IP endpoint attached to the functional VM network interface blade.
<br>
<<img width="1366" height="768" alt="Screenshot 9 Virtual Machine IP Address - VPNSyber" src="https://github.com/user-attachments/assets/b5382f58-b2a4-46ec-826d-4b2c5eaf774d" />
>
<br>
<br>

**Step 10: RDP Handshake & Login**
* Initializing a secure Remote Desktop session into the remote Windows Server environment using established local admin credentials.
<br>
<<img width="1366" height="768" alt="Screenshot 10 Logging in Virtual Machine - VPN Cyber" src="https://github.com/user-attachments/assets/21900d25-8490-4f1e-9175-4f488d9c8c39" />
>
<br>
<br>

**Step 11: Active VM Session**
* Successfully initiated the interactive GUI desktop environment inside the remote Azure VM (`VPNSD06`).
<br>
<<img width="1366" height="768" alt="Screenshot 11 Logged in to Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/ce73dcf8-9775-40c3-bb6d-367392c1e448" />
>
<br>
<br>

**Step 12: Initial VM IP Verification**
* Checked *whatismyipaddress.com* from within the VM to verify and document its default public Azure routing footprint.
<br>
<<img width="1366" height="768" alt="Screenshot 12 Virtual Macchine IP Address VPNSyber IP addresss" src="https://github.com/user-attachments/assets/01b02ef0-cf5c-42bd-847f-61b52946cb86" />
>
<br>

---

### 🔹 Phase 4: VPN Deployment & Traffic Encapsulation

**Step 13: Software Acquisition**
* Downloaded the official Proton VPN installation executable onto the remote virtual machine environment.
<br>
<<img width="1366" height="768" alt="Screenshot 13 Downloading Proton VPN on Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/97a17d63-a7e3-45f3-8503-94efd67c1046" />
>
<br>
<br>

**Step 14: Client Installation**
* Executed the setup package to install the Proton VPN service agent onto the Windows Server operating system.
<br>
<<img width="1366" height="768" alt="Screenshot 14 Installing Proton VPN on Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/6099c371-017a-4f66-96a7-2625a34a309c" />
>
<br>
<br>

**Step 15: VPN Client Launch**
* Initialized the Proton VPN application interface inside the VM, preparing for global node connection.
<br>
<<img width="1366" height="768" alt="Screenshot 15 Virtual Machine VPNSyber IP on Proton VPN" src="https://github.com/user-attachments/assets/4c0d6f82-68f2-4182-9aa7-bfd180d64863" />
>
<br>
<br>

**Step 16: Tunnel Initialization**
* Triggered the connection sequence to route the VM's internet traffic through a secure, third-party global VPN server.
<br>
<<img width="1366" height="768" alt="Screenshot 16 Connecting to Proton VPN on Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/2a296c69-80c4-4e81-bc2d-60dc83f30b70" />
>
>
<br>
<br>

**Step 17: Geographic Shift Verification**
* Re-evaluated the public IP profile within the VM browser, confirming successful data encapsulation and an updated geographical footprint.
<br>
<<img width="1366" height="768" alt="Screenshot 17 Change of IP Address Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/1b92748b-4a5e-4aa4-9fca-ddaf199c918b" />
>
<br>

---

### 🔹 Phase 5: Session Termination & Resource Lifecycle Management

**Step 18: Session Disconnection**
* Safely terminated the interactive Remote Desktop Protocol (RDP) session to the virtual machine.
<br>
<<img width="1366" height="768" alt="Screenshot 18 Closing Virtual Machine VPNCyber" src="https://github.com/user-attachments/assets/2fc89ef8-d144-4ca9-93b8-1e3ef500c0de" />
>
<br>
<br>

**Step 19: Compute De-provisioning**
* Initialized the deletion command for the virtual machine compute resource (`VPNSD06`) from the Azure Portal.
<br>
<<img width="1366" height="768" alt="Screenshot 19 Deleting Virtual Machine VPNSyber" src="https://github.com/user-attachments/assets/964eb16c-14b4-40b8-a2ec-43e15620c477" />
>
<br>
<br>

**Step 20: Compute Deletion Verification**
* Monitored the Azure control plane notifications to confirm the compute instance was completely removed.
<br>
<<img width="1366" height="768" alt="Screenshot 20 Virtual Machine Deleted" src="https://github.com/user-attachments/assets/c1f98fa1-6687-457a-989c-00ec29ef9add" />
>
<br>
<br>

**Step 21: Resource Group Takedown**
* Initialized a comprehensive deletion of the entire `dumela` logical container to catch all remaining networking components.
<br>
<<img width="1366" height="768" alt="Screenshot 21 Deleting Resource Group" src="https://github.com/user-attachments/assets/3263bdc4-a231-4327-9bc5-e910157547a2" />
>
<br>
<br>

**Step 22: Final Lifecycle Audit**
* Confirmed total destruction of all lab-associated infrastructure assets to guarantee zero ongoing credit spend.
<br>
<<img width="1366" height="768" alt="Screenshot 22 Deleted Resource Group" src="https://github.com/user-attachments/assets/c4d9f7ab-82bc-4b6e-8256-95a1769823fa" />
>
<br>

---

## 🏁 Conclusion & Key Takeaways

This lab successfully demonstrated the mechanics of public cloud architecture and network traffic manipulation through VPN tunneling. By deploying an infrastructure footprint in a remote cloud region and analyzing the resulting network routing, several foundational IT concepts were validated in a live environment:

* **Geographic IP Allocation:** Documented how public IPv4 footprints are inextricably tied to the physical data center hosting the compute infrastructure, regardless of where the administrator is physically located.
* **Encapsulation & Bypassing CDNs:** Observed firsthand how an encrypted VPN tunnel overrides the default ISP/Cloud gateway, modifying traffic paths across global Content Delivery Networks (CDNs) and altering localized web application presentation (languages, regional restrictions, and local top-level domains).
* **Lifecycle Management:** Practiced proper resource governance by auditing and completely decommissioning active cloud dependencies to prevent budget overruns and idle resource accumulation.
