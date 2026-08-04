# Remote-support-lab
Simulated remote IT support scenario using a Windows VM and RDP — diagnosing and resolving a network connectivity failure that also disrupted remote access, with full incident documentation.
# Remote Support & Troubleshooting Lab

## Overview
Simulated a real-world remote IT support scenario using a Windows 11 VM (VMware Fusion, bridged network) 
and RDP to demonstrate diagnosing and resolving a network connectivity failure remotely.

## Environment
- Host: MacBook (Apple Silicon)
- VM: Windows 11 ARM64 (VMware Fusion, Bridged Networking)
- Remote access: RDP via Windows App (Microsoft Remote Desktop)

## Incident Ticket

**Issue Reported:** User's machine lost network connectivity; remote access unavailable.

**Diagnostic Steps:**
1. Confirmed baseline network state via Network Connections (ncpa.cpl) on VM
2. Simulated failure by disabling the network adapter locally
3. Attempted RDP reconnection from host machine — connection failed, confirming loss of remote access alongside network connectivity

**Root Cause:** Network adapter disabled, cutting off both internet access and remote management capability.

**Resolution:**
1. Accessed VM via local console (VMware Fusion) since RDP was unavailable
2. Re-enabled network adapter
3. Verified network restored via ipconfig
4. Reconnected successfully via RDP from host machine, confirming full resolution

**Time to Resolution:** ~[X minutes]

## Key Takeaway
Demonstrates the importance of out-of-band/local access as a fallback when remote management 
tools themselves are affected by the issue being diagnosed — a real scenario remote support 
technicians encounter.

## Screenshots
See `/screenshots` folder for full documentation of each step.
