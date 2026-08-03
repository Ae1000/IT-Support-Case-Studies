# IT Support & System Infrastructure Case Studies 🛠️💻

Welcome to my technical documentation repository. Alongside my **Cisco Network Academy Data Analytics** milestones, this space is dedicated to logging real-world IT support interventions, system optimization workflows, and network infrastructure troubleshooting.

---

## Case Study 01: Resolving Advanced OS Network Conflicts & Peripheral Hardware Locks

### 📌 Executive Summary
A workstation running a Windows environment suffered a complete failure of its wireless routing stack following a manual Local Area Network (LAN) deployment. The system experienced severe system policy conflicts, rendering the native Mobile Hotspot engine inaccessible, missing critical virtual adapters, and locking down secondary USB peripheral controllers.

### 🛠️ The Challenge & Root Cause Analysis
* **Network Stack Corruption:** A previous configuration left a hidden legacy firewall rule (`NC_PersonalFirewallConfig`) active in the system policies. This was hard-blocking the system's underlying Internet Connection Sharing (`SharedAccess`) daemon.
* **Interface Conflict Loop:** A rogue secondary internal wireless controller (Realtek RTL8188EU) triggered an IP allocation clash with the primary adapter (Intel Wi-Fi 6 AX200), causing the modern OS settings GUI to freeze and gray out.
* **USB Port Deadlock:** Rapid hardware shifts caused the Windows Universal Serial Bus controllers to lock down power distribution to the physical USB Root Hubs, rendering input peripherals (wireless mouse) completely unresponsive.

### 🚀 Technical Intervention & Solution Strategy
1. **Phase 1: Deep Policy & Registry Purge**  
   Executed a deep network component wipe via administrative command lines (`netcfg -d`) to strip away rogue virtual adapter caches. Cleaned the Windows Registry by manually deleting the legacy firewall block to restore structural system privileges.
2. **Phase 2: Legacy Interface Bridging**  
   Bypassed the glitched, modern OS interface by forcing a direct data link within the legacy network adapter core (`ncpa.cpl`). Bound the active Intel internet stream directly to the newly initialized virtual interface card.
3. **Phase 3: Hardware Controller Restoration**  
   Uninstalled the deadlocked USB Root Hub (USB 3.0) drivers from the motherboard map. Triggered a low-level hardware scan during a clean cold-boot sequence to safely force-flash power back to all physical USB slots, instantly restoring the peripheral mouse.

### 📊 Business Outcomes & Results
* **100% Core Functionality Restored:** Workstation is fully stabilized with zero residual registry or hardware errors.
* **Automated Dual-Sharing Enabled:** Engineered a self-managing network path. The system now automatically routes high-speed data from either a physical LAN line or Wi-Fi through the hotspot bridge seamlessly.
* **Zero Downtime:** Successfully repaired deep-level OS and peripheral infrastructure anomalies without requiring a destructive operating system reinstall.

---

## 📬 Connect With Me
If you are looking for data insights, tech systems optimization, or freelance IT contract support, let's connect:
* **LinkedIn:** www.linkedin.com/in/enyinnaya-ahuekwe-48b778424
* **Email:** enyinnaya.setters@gmail.com
