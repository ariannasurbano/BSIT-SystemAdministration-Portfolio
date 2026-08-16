Week 03 — Server Installation and Configuration

Project Overview

This project focuses on installing and configuring a server operating system inside a virtual machine. The activities include server installation, basic configuration, verification, BIOS and UEFI comparison, and understanding the Linux boot process.

Learning Objectives

By completing this project, I learned how to:

- Install a server operating system in a virtual machine.
- Configure the hostname, administrator account, and basic network settings.
- Verify that the server is working correctly using commands.
- Understand the differences between BIOS and UEFI.
- Understand the major steps of the Linux boot process.
- Identify common installation problems and their solutions.

Virtual Machine Specifications

Component| Specification
Virtualization Software| Virtual Machine
Operating System| Ubuntu Server
RAM| 4 GB
Storage| 25 GB
CPU| 2 Cores
Network| NAT
Installation Media| Ubuntu Server ISO

Installation Summary

Ubuntu Server was installed inside a newly created virtual machine. The installation process included selecting the installation language, configuring the keyboard, setting up the network, creating a user account and password, selecting the storage configuration, installing the required system files, and restarting the virtual machine after installation.

After the installation was completed, the server successfully booted and displayed the login prompt.

Configuration Summary

After installation, the server was configured with the necessary basic settings. These included the hostname, user account, password, network connection, and SSH service.

The server was also updated using the following commands:

sudo apt update
sudo apt upgrade -y

Verification Results

The following commands were used to verify the server:

Hostname

hostname

The command displayed the assigned hostname of the server.

IP Address

ip addr

The command displayed the network interfaces and assigned IP address.

Internet Connectivity

ping -c 4 google.com

The server successfully tested connectivity to the internet.

SSH Service

systemctl status ssh

The SSH service was checked to verify that it was active and running.

BIOS vs UEFI Highlights

Feature| BIOS| UEFI
Boot Process| Older firmware boot process| Modern firmware boot process
Disk Support| More limited| Supports very large disks
Partition Style| Commonly MBR| Commonly GPT
Security| Basic| Supports Secure Boot
Speed| Generally slower| Generally faster
Modern Usage| Mostly legacy systems| Standard on modern computers

UEFI has largely replaced BIOS because it provides better hardware support, faster booting, support for GPT and large storage devices, and additional security features such as Secure Boot.

Embedded Boot Process Flowchart

┌─────────────┐
│  Power On   │
└──────┬──────┘
       ↓
┌──────────────────────┐
│ BIOS/UEFI Initialize │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Boot Device Detection│
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Boot Loader (GRUB) │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│     Linux Kernel     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│     init/systemd     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│    Services Start    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│     Login Prompt     │
└──────────────────────┘

Challenges Encountered

Several challenges were encountered during the virtual machine installation and configuration. One problem involved the virtual machine failing to boot because the operating system ISO was not properly mounted or selected. This was resolved by checking the virtual machine settings and selecting the correct ISO file.

Another challenge involved verifying the network connection and services. The verification commands were used to identify whether the server was properly connected and whether the SSH service was running.

These problems helped improve my understanding of virtual machine settings, installation media, and basic server troubleshooting.

Reflection

This Week 03 activity helped me understand the basic process of installing and managing a server operating system in a virtual machine. Before performing the activity, I had limited experience with server installation and configuration. Through the installation process, I learned that setting up a server requires careful attention to details such as the ISO file, virtual machine hardware, storage, network configuration, username, and password.

One of the most important things I learned was how to verify whether the server is working correctly after installation. Commands such as "hostname", "ip addr", "ping", and "systemctl status ssh" provide useful information about the server. Instead of simply assuming that the installation was successful, I learned how to check the hostname, network connection, internet connectivity, and SSH service.

I also learned the difference between BIOS and UEFI. BIOS is an older firmware system, while UEFI is the modern replacement that provides better support for large storage devices, GPT partitioning, faster booting, and security features such as Secure Boot. Understanding these differences is important because modern computers commonly use UEFI.

The boot process flowchart also helped me understand what happens after a computer is powered on. I learned that the system goes through firmware initialization, detects a boot device, loads GRUB, starts the Linux kernel, starts systemd, launches services, and eventually displays the login prompt.

Overall, the activity improved my practical skills in virtualization, Linux server installation, configuration, and troubleshooting. The challenges I encountered also taught me to check settings carefully and use verification commands instead of guessing. These skills will be useful in future system administration activities and server-related projects.

References

1. Ubuntu Documentation — Ubuntu Server installation and administration.
2. Linux manual pages — Commands and system administration references.
3. Microsoft Documentation — BIOS and UEFI concepts.
4. Ubuntu Server documentation — Server configuration and system management.
5. Class lecture materials and Week 03 laboratory instructions.Virtualization Software| Virtual Machine
Operating System| Ubuntu Server
RAM| 4 GB
Storage| 25 GB
CPU| 2 Cores
Network| NAT
Installation Media| Ubuntu Server ISO

#Installation Summary

Ubuntu Server was installed inside a newly created virtual machine. The installation process included selecting the installation language, configuring the keyboard, setting up the network, creating a user account and password, selecting the storage configuration, installing the required system files, and restarting the virtual machine after installation.

After the installation was completed, the server successfully booted and displayed the login prompt.

Configuration Summary

After installation, the server was configured with the necessary basic settings. These included the hostname, user account, password, network connection, and SSH service.

The server was also updated using the following commands:

sudo apt update
sudo apt upgrade -y

Verification Results

The following commands were used to verify the server:

Hostname

hostname

The command displayed the assigned hostname of the server.

IP Address

ip addr

The command displayed the network interfaces and assigned IP address.

Internet Connectivity

ping -c 4 google.com

The server successfully tested connectivity to the internet.

SSH Service

systemctl status ssh

The SSH service was checked to verify that it was active and running.

#BIOS vs UEFI Highlights

Feature| BIOS| UEFI
Boot Process| Older firmware boot process| Modern firmware boot process
Disk Support| More limited| Supports very large disks
Partition Style| Commonly MBR| Commonly GPT
Security| Basic| Supports Secure Boot
Speed| Generally slower| Generally faster
Modern Usage| Mostly legacy systems| Standard on modern computers

UEFI has largely replaced BIOS because it provides better hardware support, faster booting, support for GPT and large storage devices, and additional security features such as Secure Boot.

Embedded Boot Process Flowchart

┌─────────────┐
│  Power On   │
└──────┬──────┘
       ↓
┌──────────────────────┐
│ BIOS/UEFI Initialize │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│ Boot Device Detection│
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│   Boot Loader (GRUB) │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│     Linux Kernel     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│     init/systemd     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│    Services Start    │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│     Login Prompt     │
└──────────────────────┘

#Challenges Encountered

Several challenges were encountered during the virtual machine installation and configuration. One problem involved the virtual machine failing to boot because the operating system ISO was not properly mounted or selected. This was resolved by checking the virtual machine settings and selecting the correct ISO file.

Another challenge involved verifying the network connection and services. The verification commands were used to identify whether the server was properly connected and whether the SSH service was running.

These problems helped improve my understanding of virtual machine settings, installation media, and basic server troubleshooting.

#Reflection

This Week 03 activity helped me understand the basic process of installing and managing a server operating system in a virtual machine. Before performing the activity, I had limited experience with server installation and configuration. Through the installation process, I learned that setting up a server requires careful attention to details such as the ISO file, virtual machine hardware, storage, network configuration, username, and password.

One of the most important things I learned was how to verify whether the server is working correctly after installation. Commands such as "hostname", "ip addr", "ping", and "systemctl status ssh" provide useful information about the server. Instead of simply assuming that the installation was successful, I learned how to check the hostname, network connection, internet connectivity, and SSH service.

I also learned the difference between BIOS and UEFI. BIOS is an older firmware system, while UEFI is the modern replacement that provides better support for large storage devices, GPT partitioning, faster booting, and security features such as Secure Boot. Understanding these differences is important because modern computers commonly use UEFI.

The boot process flowchart also helped me understand what happens after a computer is powered on. I learned that the system goes through firmware initialization, detects a boot device, loads GRUB, starts the Linux kernel, starts systemd, launches services, and eventually displays the login prompt.

Overall, the activity improved my practical skills in virtualization, Linux server installation, configuration, and troubleshooting. The challenges I encountered also taught me to check settings carefully and use verification commands instead of guessing. These skills will be useful in future system administration activities and server-related projects.

#References

1. Ubuntu Documentation — Ubuntu Server installation and administration.
2. Linux manual pages — Commands and system administration references.
3. Microsoft Documentation — BIOS and UEFI concepts.
4. Ubuntu Server documentation — Server configuration and system management.
5. Class lecture materials and Week 03 laboratory instructions.

