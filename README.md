# Home Lab: Kali Linux Environment


## Overview:


I built a Linux environment to learn how Linux works, complete exercises in practical courses and experiment with industry cyber security tools.


## Tools Used:


- VMware Workstation Pro
- Kali Linux
- OpenVPN
- HackTheBox


## Setup Process:


### Installing VMware Workstation Pro:


I used VMware workstation pro 26H1 which has become free to use. IT professionals may use VMware workstation as it offers strong performance and powerful features.


The setting up process of VMware Workstation Pro is very simple. After making an account and filling out your details, you can download and run the installer file (exe for Windows)


### Installing Kali Linux:


I chose Kali Linux because it contains powerful tools used in cyber security out of the box. Installation also caused the least amount of issues which is important for beginners.






I chose to install the "installer images" as they give more configuration options during the installation process.


### Setting up the VM:






On VMware Workstation Pro, because I chose the installer image from the Kali Linux website, I have to "Create a new Virtual Machine".






VMware was unable to identify Kali Linux automatically, so I chose Debian 13.x 64-bit as Kali Linux is based on Debian rolling release and this was the closest option available.






After configuration, I gave 4 cores, 6gb RAM, 30gb of NVME storage (matches host drive type) and 2GB of graphics memory to the system (Accelerate 3D Graphics on). This should be more than enough for the system.






I used NAT (Network Address Translation) which allows my VM to "borrow" my IP address to send and receive data when required, but keeps the VM isolated so other devices on the network cannot find it, which is a security advantage.


### Configuring Kali Linux Installation:






When I first booted up the OS, I was presented with several options. "Graphical Install" is the easiest and most straightforward way to configure our installation for Kali Linux.






After choosing things like the language, keyboard layout and username, I was presented with which drive I want to install Kali Linux to.






After Kali Linux downloads the core system, it presents a range of "extras" to install. For my desktop environment, I chose XFCE because of its lightweight nature which makes it suitable for a VM.






After choosing options, Kali Linux installs. I also installed the GRUB Bootloader to our Kali Linux drive so the system can boot up correctly. After that, the installation is complete and I can reboot (it will reboot into my actual virtual drive with Kali Linux)






This is our Kali Linux XFCE environment booted up and running on my VM for the first time.


## Configuring Kali Linux:






Kali Linux comes with a lot of tools preinstalled including SSH and openVPN. The screenshot above shows Brave browser (my preferred option) and a terminal window which shows the important tools I will need preinstalled.


## Hack The Box: Linux Fundamentals:


As a beginner, I am currently progressing through HTB: Linux Fundamentals to learn more about Linux. My home lab allows me to experiment with the commands and complete the exercises.






Before I can do the exercises, HTB requires to connect to a VPN and then SSH into the target system.


- "cd Downloads" puts me in the location of the downloaded HTB VPN file
- "sudo openvpn academy-regular.ovpn" allows me to connect to the VPN. It is shown on the top right of the screenshot
- on the bottom terminal, "ssh htb-student@10.129.67.86" with the HTB provided password allows me to SSH into the target system, where I can type my commands to get the answers to the exercises

