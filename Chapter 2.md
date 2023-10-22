## Exploring the Basics: Key Terminologies and Platforms

---

In our journey into the realm of robotics and cybersecurity, understanding the underlying platforms and terminologies is indispensable. This chapter aims to elucidate some basic yet crucial terms and platforms that will set the foundation for the topics to follow.

### Linux vs Windows

At the core of any computer system lies its operating system (OS), a software that manages all hardware resources and provides various services for computer programs. Two of the most prevalent operating systems are Linux and Windows.

- **Windows**: With its user-friendly interface, Windows caters to a broader audience. It's a closed-source operating system with robust support for a plethora of applications, making it a popular choice among both home and enterprise users.

- **Linux**: Known for its stability, security, and flexibility, Linux is a favorite among developers and cybersecurity professionals. It's an open-source operating system, meaning its code is accessible to anyone, encouraging community-driven development and support.


### Virtual Machines

Delving into cybersecurity practices often requires a safe, isolated environment, which is where Virtual Machines (VMs) come into play. A VM is a software emulation of a computer system, running on top of a physical host machine. Some notable VM platforms include:

- **Hyper-V**: Exclusive to Windows Pro users, Hyper-V allows for the creation and management of virtual machines. To check if you have Hyper-V, type "Turn Windows features on or off" in the search bar, and look for Hyper-V. If your edition doesn't have Hyper-V, you can upgrade to Windows Pro.

- **VirtualBox and VMware**: These are cross-platform solutions that support the creation of VMs on both Linux and Windows hosts.

- **Dual Boot vs Live Boot**: Dual booting involves installing multiple operating systems on a single machine, each having its dedicated partition. Live booting, on the other hand, allows you to run an OS from a USB stick or CD, without installation. For dual booting, every time you turn on your computer you will have a choice between going into Windows or Linux, or whatever combinations of operating systems you have installed.

### Kali Linux

In the cybersecurity domain, Kali Linux stands out as a dedicated environment loaded with tools for penetration testing and digital forensics. Its extensive toolkit and community support make it a go-to platform for many security professionals.

### Windows Subsystem for Linux (WSL)

For those ingrained in the Windows ecosystem, diving into Linux-based tools may seem daunting. However, Windows Subsystem for Linux (WSL) bridges this gap by allowing Linux distributions to run alongside your Windows installation, providing a convenient platform to explore Linux-based tools and utilities. I'd highly recommend learning about WSL even as a side platform due to having easy access to all the tools and commands that windows can't support natively.


When it comes to virtualization, Virtualbox/Vmware - I personally prefer Hyper-V. If you have windows pro or for a few dollars upgrade - it allows for windows native virtual machine emulation and will be much faster to run and interact with.

Keep in mind you may need to enable virtualization in your computers BIOS before virtual machines work on your system.

https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html
https://www.virtualbox.org/
https://www.kali.org/


Making USBs:
https://rufus.ie/en/
https://sourceforge.net/projects/win32diskimager/
https://unetbootin.github.io/
https://etcher.balena.io/