# **〽 How to install snort on kali:**
![](./snort.png)
## **〽What is snort :**

- Snort is the foremost Open Source Intrusion Prevention System (IPS) in the world.
- Snort IPS uses a series of rules that help define malicious network activity and uses those rules to find packets that match against them and generates alerts for users.
- Snort can be deployed as :
  1. a packet sniffer like tcpdump.
  2. a packet logger — which is useful for network traffic debugging.
  3. full-blown network intrusion prevention system.

### 1. **Firstly :**
    - mkdir snort-ressources
    - sudo apt-get update
    - apt-get install mingw-w64
### 2. **Install bison and flex :**
    apt-get install -y bison flex

### 3. **Download and install daq :**
```bash
- wget https://www.snort.org/downloads/snort/daq-2.0.7.tar.gz
- tar -xvzf daq-2.0.7.tar.gz
- cd daq-2.0.7
- ./configure && make && sudo make install
```  
### 4. **Install some dependecies:**
    sudo apt-get install -y libpcap-dev gcc make libpcre3-dev zlib1g-dev libluajit-5.1-dev openssl libssl-dev libnghttp2-dev libdumbnet-dev

### 5. **Download & Install pcre:**
```bash
- wget https://github.com/PCRE2Project/pcre2/releases/download/pcre2-10.40/pcre2-10.40.tar.gz
- tar -xvzf prcre2–10.40.tar.gz
- cd pcre2–10.40
- ./configure && make && sudo make install
```
### 6. **Install LuaJIT:**
```bash
- wget https://luajit.org/download/LuaJIT-2.0.5.tar.gz
- tar -xvzf LuaJIT-2.0.5.tar.gz
- cd LuaJIT-2.0.5
- make && sudo make install
```
### 7. **Install Snort:**   
```bash
- wget https://www.snort.org/downloads/snort/snort-2.9.20.tar.gz
- tar -xvzf snort-2.9.20.tar.gz
- cd snort-2.9.20
- ./configure CPPFLAGS="-I/usr/include/tirpc" --enable-sourcefire && make && sudo make install
 ```
### 8. **libpcap error:**
    - locate libpcap:
	       /usr/lib/x86_64-linux-gnu/libpcap.so.1.10.1 
    - sudo ln -s libpcap.so.1 libpcap.so.1.10.1 
    
## **✅ Now snort is successfully installed**

```bash 
    kali@kali$ snort -v

    Running in packet dump mode

            --== Initializing Snort ==--
    Initializing Output Plugins!
    pcap DAQ configured to passive.
    Acquiring network traffic from "eth0".
    Decoding Ethernet

            --== Initialization Complete ==--

    ,,_     -*> Snort! <*-
    o"  )~   Version 2.9.20 GRE (Build 82) 
    ''''    By Martin Roesch & The Snort Team: http://www.snort.org/contact#team
            Copyright (C) 2014-2022 Cisco and/or its affiliates. All rights reserved.
            Copyright (C) 1998-2013 Sourcefire, Inc., et al.
            Using libpcap version 1.10.1 (with TPACKET_V3)
            Using PCRE version: 8.39 2016-06-14
            Using ZLIB version: 1.2.11
    
```
### **Ressources :**
- [Link 1](https://koayyongcett.medium.com/snort-installation-in-kali-linux-from-the-source-9a005558a2ea)
- [Link 2](https://www.systranbox.com/how-to-install-snort-on-kali-linux/) 
- [Link 3](https://docs.napatech.com/r/Running-Open-Source-Libraries-and-Applications-with-Napatech-SmartNICs/Snort-Installation-and-Configuration)
- [pcre2](https://github.com/PCRE2Project/pcre2/releases)
- [luajit](https://luajit.org/download.html)
- [#error Only Win32](https://unix.stackexchange.com/questions/329122/is-this-error-only-win32-target-is-supported-coming-from-wrong-cc1plus)
- [Snort-install-Dependency-resolve](https://topic.alibabacloud.com/a/snort-install-dependency-resolve_8_8_31275138.html)
- [Snort Official Website](https://www.snort.org/)

#by Goblo
