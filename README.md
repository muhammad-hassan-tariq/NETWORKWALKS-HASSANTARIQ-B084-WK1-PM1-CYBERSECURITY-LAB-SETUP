# Cybersecurity Lab Setup — Week 1, PM1

**Name:** Muhammad Hassan Tariq
**Batch:** B084

## Objective
Set up an isolated virtual lab environment using VirtualBox and Kali Linux, with a
custom NAT Network, ready for upcoming cybersecurity lab exercises.

## Steps

### Step 1: Install 7-Zip
Downloaded and installed 7-Zip to extract the Kali Linux archive.

### Step 2: Install VirtualBox
Downloaded and installed Oracle VirtualBox on Windows.

### Step 3: Create a NAT Network
Created a custom NAT Network in VirtualBox (`File > Tools/Preferences > Network >
NAT Networks`) with:
- Name: `KaliNatNetwork`
- IPv4 Prefix: `10.0.0.0/24`
- DHCP enabled

![NAT Network settings<img width="1093" height="930" alt="natnetwork" src="https://github.com/user-attachments/assets/c779cfe9-38d1-4838-b216-4fc85e60a1c7" />


### Step 4: Import Kali Linux VM
Downloaded the Kali Linux VirtualBox image from kali.org, extracted it with 7-Zip,
and imported it into VirtualBox via `File > Import Appliance`.

![Kali VM imported]<img width="1025" height="936" alt="kalilinux-import" src="https://github.com/user-attachments/assets/be7f8d0c-b5c3-476e-b911-2a8e7cc0219c" />

### Step 5: Configure Kali's IP
Attached the Kali VM's network adapter to the NAT Network created in Step 3.
Verified the IP configuration and internet connectivity:
ip a
ping -c 4 google.com

Kali received IP `10.0.0.3/24` via DHCP, and connectivity was confirmed with 0% packet loss.

![IP configuration and ping test]<img width="1275" height="801" alt="ip-ping" src="https://github.com/user-attachments/assets/caafc40b-fa3f-44b7-a084-b15d219c30d8" />


### Step 6: Take a Snapshot
Took a VirtualBox snapshot of the configured Kali VM as a clean baseline to restore
to if needed later.

![Snapshot taken]<img width="1057" height="373" alt="snapshot-taken" src="https://github.com/user-attachments/assets/2f9f4d17-01e5-4da8-b3a9-2e87cdbd4249" />


## Notes
No issues encountered. Internet connectivity through the NAT Network was confirmed
working correctly.

