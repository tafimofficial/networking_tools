# Networking Master Pro (Android C NDK + Modern Animated App)

An enterprise-grade, high-performance Android application built with a **Pure C NDK Core** (`arm64-v8a`, `armeabi-v7a`, `x86_64`) and a **Hardware-Accelerated 60FPS SaaS Animated Dynamic UI**. Supports **Android 10 (API 29) and higher (up to Android 14/15, API 34+)**.

---

## 🌟 Key Architecture & Highlights

1. **Pure C NDK Core (`/app/src/main/cpp/`)**:
   - `network_core.c` / `network_core.h`: High-speed bitwise IP math, CIDR mask generation, host range calculation, wildcard masking, and RFC 1071 16-bit one's complement checksum calculation.
   - `packet_engine.c` / `packet_engine.h`: OSI 7-layer PDU structure, frame encapsulation/decapsulation, ICMP ping sequence generator, and TCP port scanner engine.
   - `cli_engine.c` / `cli_engine.h`: State-machine based command parser for Cisco IOS and MikroTik RouterOS with context-aware command validation and prompt switching.
   - `native_bridge.c`: JNI bindings connecting the C engine directly to Android Java and WebView via `AndroidNativeBridge`.
   - `CMakeLists.txt`: Standard CMake build system targeting Android NDK.

2. **Complete Syllabus Coverage (Bangla & English)**:
   - **All 10 Syllabus Modules + Modern Extra Topics**:
     1. Introduction to Networking (PAN, LAN, WLAN, MAN, WAN, SAN, Topologies, Client-Server vs P2P)
     2. Network Models (OSI 7 Layers, TCP/IP 4 Layers, PDU Encapsulation)
     3. Physical Layer & Media (UTP/STP Cat5e-Cat8, SMF/MMF Fiber, SFP+, Wi-Fi 6/6E/7)
     4. Data Link Layer & Switching (MAC OUI, ARP & Gratuitous ARP, VLAN 802.1Q, STP/RSTP, LACP EtherChannel)
     5. Network Layer & IP Addressing (IPv4 Classes, RFC 1918 Private ranges, Subnetting, VLSM, CIDR, IPv6, ICMP)
     6. Routing (Routing table logic, Static, Default, OSPF Single/Multi-area, BGP eBGP/iBGP, FHRP HSRP/VRRP/GLBP)
     7. Transport Layer (TCP 3-Way Handshake, Flow Control, Sliding Window, UDP, Well-Known Ports)
     8. Network Services & Application Layer (DNS Records, DHCP DORA process, NAT & PAT Overload)
     9. Network Security (CIA Triad, Stateful vs NGFW, Standard/Extended ACL, IPsec/SSL VPN, Layer 2 Port Security/DAI/DHCP Snooping)
     10. Advanced Networking & Modern Tech (SDN Controllers, SD-WAN, Cloud AWS VPC/Azure VNet, Python Automation Netmiko/Paramiko, Ansible, Zero Trust)
   - Real-time search filter to find any concept or protocol instantly.

3. **Segment 2: Practice & Live Testing Labs**:
   - **Subnet & VLSM Lab**: Instant IP calculation, usable host ranges, and multi-department VLSM table planner with binary bitwise visualizer.
   - **Live ICMP Ping Simulator**: Real-time canvas latency curve, sequence numbers, jitter, and packet drop simulation.
   - **Interactive Port Scanner**: Live TCP/UDP service scanner with port banners (SSH, HTTP, HTTPS, MySQL, BIND DNS, RDP).
   - **7-Layer OSI Encapsulation Simulator**: Visual step-by-step PDU wrapping from Layer 7 (Data) down to Layer 1 (Physical Bits).
   - **Interactive Network Topology Canvas**: Moving data packets between PC1, Switch, Router, Firewall, and Web Server with live event logs and firewall block simulations.

4. **Segment 3: Configurable Devices & Interactive CLI Terminal**:
   - Cisco IOS & MikroTik RouterOS console simulator (`Router>`, `Router#`, `Router(config)#`, `Router(config-if)#`).
   - **Command Inspector**: Displays real-time explanations for each command (বাংলায় উদ্দেশ্য, সিনট্যাক্স ব্রেকডাউন ও ইন্ডাস্ট্রি বেস্ট প্র্যাকটিস টিপস).
   - **1-Click Configuration Presets**:
     * Cisco VLAN Creation & 802.1Q Trunk Setup
     * Cisco OSPF Single Area Dynamic Routing
     * Cisco NAT Overload (PAT) for Internet Access
     * Cisco Port Security MAC Hardening
     * MikroTik Internet Gateway & DHCP Server Setup

---

## 🚀 How to Run & Build

### 1. Instant Live Preview (Browser / Mobile Wi-Fi)
```bash
npm start
```
Open `http://localhost:3000` in any web browser or open `http://<YOUR_PC_IP>:3000` on your Android phone connected to the same Wi-Fi.

### 2. Android Studio & APK Build (Android 10+)
1. Open **Android Studio** (Hedgehog, Iguana, Koala or newer).
2. Choose **Open an Existing Project** and select the folder:
   `c:\Users\T\Downloads\networking\android_ndk_app`
3. Ensure Android NDK (version 25+ or 26+) and CMake (3.22.1+) are installed via SDK Manager.
4. Click **Build -> Build Bundle(s) / APK(s) -> Build APK(s)**.
5. The compiled APK will be generated at:
   `app/build/outputs/apk/debug/app-debug.apk`
6. Install on any Android 10+ phone, tablet, or emulator:
   ```bash
   adb install app-debug.apk
   ```
