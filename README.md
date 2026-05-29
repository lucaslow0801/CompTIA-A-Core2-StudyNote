# 🖥️ CompTIA A+ Core 2 Study Notes

> **Exam:** CompTIA A+ Core 2 (220-1102)
> A comprehensive study guide covering Operating Systems, Security, Software Troubleshooting, and Operational Procedures.

---

## 📋 Table of Contents

| Domain | Title |
|--------|-------|
| 1.0 | [Operating Systems](#10-operating-systems) |
| 2.0 | [Security](#20-security) |
| 3.0 | [Software Troubleshooting](#30-software-troubleshooting) |
| 4.0 | [Operation Procedures](#40-operation-procedures) |

---

---

## 1.0 Operating Systems


### 1.1 Operating system (OS) types


> 💡 **Key Tip:** Home Client - Designed for individuals and very small teams (Window home) Business Client - Designed for organizations that need to manage many users centrally (Window pro or enterprise) Open-Source and Close-Source


**Workstation systems (OSs)**


#### 1. Windows

  - Major market presence
  - A graphical operating system developed and published by
  - Microsoft
  - Use in business environments due to its strong compatibility with enterprise applications, management tools, and network infrastructure
  - Many version - Window XP, Vista, 7, 8 ,10, 11

#### 2. Linux

  - 3 main type system include Red Hat, Debian, SUSE (Ubuntu base on
  - Debian based distribution, RHEL and Fedora based on Red Hat)
  - Frequently use command-line tools
  - Works on wide variety of hardware
  - Fully open-source platform for building and testing applications

#### 3. macOS

  - Desktop OS running on Apple hardware macOs is considered a proprietary piece of software

#### 4. ChromeOS

  - ChromeOS is a proprietary operating system created by Google based on Linux
  - Operating system designed for lightweight
  - Low-cost laptops optimized for web-based applications
  - ChromeOS is a very stripped-down operating system, this made it secure and instant boot up in second

**Mobile OSs**


#### 1. iPadOS

  - Operating system for Apple's iPad tablets

#### 2. iOS

  - mobile operating system run on iPhone
  - Only install App from App Store

#### 3. Android

  - Open-source OS, based on Linux
  - A mobile OS run by device manufacturers
  - Apps installable from third-party sources, High level of customization
- Various filesystem types

> 💡 **Key Tip:** Linux typically uses ext4 and XFS. Windows primarily uses NTFS for system drives and exFAT for external storage. Modern macOS uses APFS (Apple File System) for solid-state drives (SSDs). For cross-platform compatibility (using a USB drive on all three), exFAT is the best option. Android OS use ext4, IOS use APFS


#### 1. New Technology File System (NTFS) - Window

  - Microsoft-developed file system
  - Provides advanced features such as file and folder permissions, encryption, compression, and support for very large files and partitions

#### 2. Resilient File System (ReFS) - Window Server

  - Update to NTFS, It is intended for Windows Server and Enterprise environments.
  - Support for very large drives and storage arrays
  - Self-repairing, ongoing integrity checks - no more chkdsk! provides RAID-like redundancy

#### 3. File Allocation Table 32 (FAT32) - Window, MacOS, Linux

  - Maximum File Size: 4 GB. You cannot store a single file larger than
  - 4GB
  - Max Partition Size: 32 GB
  - It works with Windows (all versions), macOS, Linux, gaming consoles (PS4/Xbox), and older hardware like digital cameras

#### 4. Extensible File Allocation Table (exFAT) - Window, MacOS, Linux

  - Large File Support: 128 PB (Petabytes)
  - Compatible across many operating systems like Windows, Linux, macOS

#### 5. Fourth extended filesystem (ext4) - Linux and android OS

  - Mostly used by Linux and android OS ext4 is a journaling file system - If the system crashes or loses power, it uses this log to recover quickly without corrupting the entire disk.
  - Case-sensitive file naming, file.txt and File.txt are treated as different files.

#### 6. Extended filesystem (XFS) - Linux

  - Supported in most Linux distributions
  - High-performance, high-capacity, and enterprise-grade.
  - Cannot Shrink Volume
  - Built-in journaling like ext4

#### 7. Apple File System (APFS) - MacOS

  - The default macOS file system optimized for SSDs and encryption
  - Snapshots: If a software update goes wrong, the system can revert to a snapshot almost instantly.
  - Encryption: APFS has native support for multi-key encryption
  - SSD: APFS is built for Solid State Drives. it uses "wear leveling" logic to increase the lifespan of your flash storage.

**Vendor life-cycle limitations**


#### 1. End-of-Life (EOL)

  - Vendor no longer markets, sells, or provides technical support for a product.

#### 2. Updating Limitation

  - Even if a product hasn't reached EOL, it may face limitations in receiving updates due to hardware constraints.
  - Hardware Requirements: A modern OS (like Windows 11) requires specific hardware (like TPM 2.0)
  - Driver Availability: Sometimes a vendor stops writing drivers for new operating systems.

#### 3. Compatibility concerns between operating systems

  - Sharing data between different OS use exFat

### 1.2 OS installations and upgrades


**Boot Method**


#### 1. Universal Serial Bus (USB)


#### 2. Network

  - PXE (Preboot eXecution Environment) - Pronounced "pixie”
  - Perform a remote network installation
  - Large-scale office deployments

#### 3. Solid-state/flash drives

  - used as fast, portable bootable devices

#### 4. Internet-based

  - Primarily suited for single users, remote workers, or when local network infrastructure is not available
  - The Recovery Partition: A small, hidden section of your internal drive used to restore the computer to factory settings if the main OS fails.
  - MacOS recovery: Download the OS directly from Apple’s servers.

#### 5. External / hot swappable drive

  - the drive can be plugged in or removed while the system is running
  - (common in servers or high-end workstations).

#### 6. Internal hard drive

  - Install and boot from separate drive
  - Accessing a specific Function key (F11/F12)

#### 7. Multiboot

  - Pick from two or more operating systems from a boot menu
  - The Boot Manager: When you turn on the computer, a menu appears (like the Windows Boot Manager or GRUB for Linux) asking which OS you want to load.

**Types of installation**


#### 1. Clean install

  - removes all existing data on the selected target partition

#### 2. Upgrade (in-place upgrade)

  - Maintain existing applications and data
  - Data keep

#### 3. Image deployment

  - Deploy a clone on every computer
  - Can be completely automated

#### 4. Remote network installation

  - Local server or shared drive
  - Install across the Internet set up a server with a centralized OS image and uses DHCP and
  - TFTP to deliver boot instructions

#### 5. Zero-touch deployment

  - no manual input at any stage, fully automating OS deployment across multiple systems
  - Example situation: The PC is shipped to the employee, they log in with their email, and the server automatically pushes the OS configuration and apps.

#### 6. Recovery partition

  - Hidden partition with installation files

#### 7. Repair installation

  - Fix problems with the Windows Os
  - Data keep

#### 8. Other considerations

  - Third-party drivers - Load alternate third party drivers when necessary (Disk controller drivers, RAID drivers, NVMe drivers, etc)

**Partitioning**


#### 1. GUID [globally unique identifier] Partition Table (GPT)

  - The modern standard. Use by UEFI
  - Can have up to 128 partitions
  - Maximum partition size is over 9 billion TB

#### 2. Master boot record (MBR)

  - The legacy standard. Use by BIOS
  - Maximum 4 primary partitions
  - Maximum partition size of 2 TB

**Drive format**


**Quick Format - Creates a new file table but does not erase the data on**


**the disk**


**Full Format - Completely wipes the data and, most importantly, scans**

- the entire partition for bad sectors.

**Upgrade considerations**


#### 1. Backup files and user preferences

  - Data Backup: Use external drives, NAS, or cloud storage
  - (OneDrive/Google Drive) to save documents, photos, and desktop files.
  - User Preferences: Don't forget browser bookmarks, saved passwords, Wi-Fi profiles, and desktop customizations.

#### 2. Application and driver support/ backward compatibility

  - Legacy Apps: Older 32-bit applications might not run correctly on newer 64-bit-only operating systems.
  - Compatibility Mode: Windows has a built-in "Compatibility Tab" in file properties that allows you to trick an app into thinking it’s running on an older version of Windows.

#### 3. Hardware compatibility

  - The "Big Three" Requirements - CPU, RAM, Storage
  - Modern Requirements - TPM 2.0, Secure Boot

**Feature updates**


**Annual update with new features**

- Used to occur every three to five years

### 1.3 Microsoft Windows editions


**Windows 10 editions**


#### 1. Home

  - home user, a student, or a very small business (1–2 people)
  - A Key Features: Includes Microsoft Edge, Cortana, and Windows
  - Hello.
  - No BitLocker (Full-disk encryption)
  - No Group Policy Management
  - No Remote Desktop Host (You can use it to control other PCs, but other PCs cannot control a "Home" machine)
  - RAM Limit: 128 GB.

#### 2. Pro

  - small-to-medium business (SMB) or a "Power User" who needs security and remote access
  - The business version of Windows. Includes everything in Home
  - Join a Domain
  - BitLocker (Full-disk encryption)
  - Windows Information Protection (WIP)
  - Group Policy Management: Includes Group Policy Editor
  - ( gpedit.msc ), allowing administrators to set "rules" for the computer
  - Remote Desktop host: Allow remote into this PC
  - RAM Limit: 2 TB

#### 3. Pro for Workstation

  - scientist, a video editor, or an engineer working with massive data sets and high-end hardware supports the Resilient File System (ReFS) by default.
  - Supports up to 4 Physical CPUs
  - RAM Limit: 6 TB of RAM.

#### 4. Enterprise

  - You are an IT Administrator for a large corporation (e.g., a bank, a hospital, or a global firm)
  - Volume License support AppLocker - Control what applications can run
  - Support Cache - Remote site file caching
  - RAM Limit: 6 TB of RAM.

**Windows 11 editions**


#### 1. Home

  - Design for Home user
  - An upgrade to Windows 10
  - No support for 32-bit CPUs
  - Internet Required for Setup
  - Security: It includes Device Encryption, but it lacks the full management suite of BitLocker
  - RAM Limit: 128 GB of RAM.

#### 2. Pro

  - Design for Business
  - BitLocker
  - Domain Join /Active Directory (AD) Domain - Allow PC become domain or manage via cloud
  - Windows Information Protection (WIP) - Protect important data leaks
  - Remote Desktop Host - Allow remote into this PC
  - RAM Limit: 2 TB of RAM.

#### 3. Enterprise

  - Design for large-scale organizations
  - Volume Licensing
  - Advanced Security - includes Microsoft Defender Application Guard, which isolated hardware-based container
  - Device management - MDM, MAM
  - BranchCache - help save bandwidth by caching data locally
  - AppLocker - Control pc which can run on company
  - Support Resilient File System (ReFS) - File system same as Window
  - Server
  - RAM Limit: 6 TB of RAM.
- N versions

**Europe version**


**“N” = Not with Media Player**

- Window 10 / 11

**Feature differences**


#### 1. Domain vs. workgroup

  - Workgroup (Home/Small Office):
  - Decentralized: Every PC is equal.
  - Stored locally on each individual PC.+
  - Hard to manage more than 20 PCs.
  - Managed PC by PC (Weak).
  - Peer-to-Peer (P2P) architecture
  - Domain (Corporate):
  - Centralized: Managed by a Server.
  - Stored centrally in Active Directory.
  - Can manage thousands of PCs.
  - Managed via Group Policy (Strong).
  - Client-Server architecture

#### 2. Desktop styles/user interface


##### a. Home


##### b. Work

  - Standard UI - Taskbar, Start Menu, and Settings app
  - Management UI - Only Pro and Enterprise editions, advanced management consoles like Computer Management ( compmgmt.msc ) and Local Users and Groups ( lusrmgr.msc ).

#### 3. Availability of Remote Desktop Protocol (RDP)

  - RDP Client: All versions (even Home) can be used to remote into another computer.
  - RDP Host: Only Pro and Enterprise can be remoted into.

#### 4. Random-access memory (RAM) support limitations

  - Home - 128 GB
  - Pro - 2TB
  - Pro for Workstations / Enterprise - 6TB

#### 5. BitLocker

  - Availability: Pro, Enterprise, and Pro for Workstations
  - Function: It encrypts the entire drive to protect data if the device is stolen. It often works with the TPM (Trusted Platform Module) chip on the motherboard

> 💡 **Key Tip:** Home Edition: Does not have BitLocker; it only has a basic version called "Device Encryption" which is much less customizable.


#### 6. gpedit.msc (Group Policy Editor)

  - Enables administrative control of desktop and user interface settings for all users on a device
  - Type in command to opens the Local Group Policy Editor
  - Function - on/off toggle setting over multiple PC once (e.g., "Disable the camera," "Force a specific wallpaper," or "Prevent users from accessing the Control Panel").

> 💡 **Key Tip:** Availability: Pro and Enterprise only. Home users must manually edit the Registry ( regedit ), which is much more dangerous and tedious.

- Upgrade paths

#### 1. In-place upgrade

  - Everything. Your applications, user files (photos, documents), desktop wallpapers, and settings are preserved.

#### 2. Clean install

  - Deleted everything
  - Stability & Fresh Start

**Hardware requirements**


#### 1. Trusted Platform Module (TPM)

  - provides a hardware-based security
  - BitLocker work with TPM to ensure that the drive cannot be read if it is moved to a different computer

#### 2. Unified Extensible Firmware Interface (UEFI)


**Feature                  Legacy BIOS            Modern UEFI**

  - MBR (Master Boot       GPT (GUID Partition

**Partition Style**

  - Record)                Table)

**Max Drive Size           2.2 TB                 9.4 ZB (Zettabytes)**

  - Secure Boot & TPM

**Security                 None**

  - Support

**Boot Speed               Slower (Sequential)    Faster (Parallel)**

- Windows 11               Not Supported          Required

### 1.4 Microsoft Windows operating system features

and tools
Task Manager

#### 1. Processes

  - Lists all active applications and background processes.
  - CPU, Memory, Disk, Network
  - End Task if app no responding

#### 2. Performance

  - Provides real-time graphs of your hardware utilization.

#### 3. Startup

  - Manage which programs startup when log in PC
  - Enable or Disable

#### 4. User

  - Shows which user accounts are currently logged into the PC

#### 5. Service

  - Background processes
  - You can right-click a service to Start, Stop, or Restart it.
  - Example: If a user can't print, restarting the "Spooler" service here is a common fix.
- Microsoft Management Console (MMC) snap-in

> 💡 **Key Tip:** Custom toolbox


#### 1. Event Viewer (eventvwr.msc)

  - To see a log of every significant event (Success, Warning, or Error) that has happened on the PC
  - Key Logs:
  - System: OS-related errors (e.g., a driver failed to load).
  - Application: Software-related issues (e.g., Photoshop crashed).
  - Security: Login attempts (Success/Audit Failure).
  - System logs categorize
  - Information - normal system operations
  - Warning - highlight non-critical issues (low disk space or driver compatibility warnings)
  - Error - serious problems (application failures or unexpected service interruptions)
  - A+ Scenario: A user says their PC "randomly restarted" at 2:00 PM.
  - You check Event Viewer to see what happened at that exact time.

#### 2. Disk Management (diskmgmt.msc)

  - Create partitions, format drives, assign drive letters, and initialize new disks
  - A+ Scenario: You install a new 2 TB SSD, but it doesn't show up in
  - File Explorer. You go here to Initialize and Format it.

#### 3. Task Scheduler (taskschd.msc)

  - Set a specific program or script to run at a certain time or when a certain event occurs
  - A+ Scenario: A company wants their antivirus to perform a full scan every Sunday at 3:00 AM.

#### 4. Device Manager (devmgmt.msc)

  - Manage hardware drivers.
  - Icons to Know:
  - Yellow Exclamation Mark (!): Driver is missing or not working correctly.
  - Down Arrow: The device is disabled.
  - A+ Scenario: The webcam isn't working. You go here to Update
  - Driver or Roll Back Driver if a recent update broke it.

#### 5. Certificate Manager (certmgr.msc)

  - View and manage digital certificates used for website encryption
  - (SSL/TLS) and secure emails.
  - A+ Scenario: A user gets a "This connection is not private" error on every website. You check here to see if a root certificate has expired.

#### 6. Local User and Groups (lusrmgr.msc)

  - Create new local users, reset passwords, or add a user to the
  - "Administrators" group.
  - A+ Scenario: A user is locked out because of too many wrong password attempts. A technician uses this to Unlock the account.

#### 7. Performance Monitor (perfmon.msc)

  - Collects long-term data (logs) on system performance. Unlike Task
  - Manager (which is real-time), this can record data over 24 hours to find patterns.
  - A+ Scenario: You suspect a "memory leak" that only happens after
  - 4 hours of use. You set a Data Collector Set in PerfMon to track it.

#### 8. Group Policy Editor (gpedit.msc)

  - To manage hundreds of OS settings from one spot.
  - A+ Scenario: You want to disable the "Run" command or hide the
  - Control Panel for all users on a specific computer. (Disable a
  - Windows feature)

> 💡 **Key Tip:** Local Group Policy Editor - Manages the local device

- Additional tools

#### 1. System Information (msinfo32. exe)

  - Provides a massive, read-only list of every hardware and software component in the system.

> **Scenario:** You need to find the exact model of a motherboard
  - without opening the case to buy compatible RAM.

#### 2. Resource Monitor (resmon.exe)

  - Provides deep, granular details about how your hardware is being used.

> **Scenario:** Task Manager shows 100% Disk usage, but you can't see
  - why. You open Resource Monitor to find that a specific antivirus scan is currently locking the C:\Windows folder.

#### 3. System Configuration (msconfig. exe)

  - To manage how the computer boots and which services run at startup
  - Key Tabs:
  - General: Choose "Diagnostic Startup" (loads only basic devices) to see if a driver is causing crashes.
  - Boot:
  - Safe boot - minimal driver environment to troubleshoot issues
  - Boot log - collects detailed information about the startup process
  - Selecting the default operating system
  - Limits on hardware resources (RAM, Processor in advance options)
  - Services: "Hide all Microsoft services" to find third-party programs causing conflicts.

#### 4. Disk Cleanup (cleanmgr.exe)

  - Safely deletes unnecessary files to free up space.
  - Targets: Temporary files, Recycle Bin, Windows Update logs, and the Windows old folder after an upgrade.

> **Scenario:** A user’s drive is 99% full, causing the system to slow
  - down. You run this to clear 15 GB of "Temporary Internet Files."

#### 5. Disk Defragment (dfrgui.exe)

  - Reorganizes data so it can be read faster.
  - SDD never defragment, otherwise it wastes lifespan
  - HDD (Hard Drives): It moves pieces of files closer together
  - (Defragment).

> **Scenario:** A mechanical hard drive is taking a long time to open
  - folders.

#### 6. Registry Editor (regedit.exe)

  - A hierarchical database that stores all settings for the OS and applications
  - Structure: Made of Hives (folders) and Keys/Values (settings)
  - Warning: There is no "Undo" in the Registry. If you delete the wrong key, Windows might not boot

> **Scenario:** You need to change a deep system setting that isn't
  - available in the Control Panel or Group Policy.

### 1.5 Microsoft command-line tools

- Summary

> 💡 **Key Tip:** help [command]   or [command] /? to check more information cls   = clear command list Command-line                   Description cd                             used for directory traversal used to list all files and subdirectories in the dir current directory locate all .exe files within a directory, dir /s *.exe including those in its subdirectories used to display TCP/IP configuration ipconfig settings used for displaying the full TCP/IP ipconfig /all configuration information for all adapters ipconfig /release              refresh the DHCP configuration for all ipconfig /renew                network adapters used for checking the reachability of a ping remote network host • Displaying active TCP/IP connections netstat • Displaying network protocol statistics display all active TCP/UDP connections and netstat -a listening ports displays addresses and port numbers in netstat -n numerical form view the name of the application associated netstat -b with each active connection or listening port • resolves a domain name to an IP address nslookup                       • used for troubleshooting DNS-related problems used to manage connections to network net use resources tracert                        tracks and displays the route taken by IP packets on their way to another host ! This information is useful for identifying

  - network bottlenecks, diagnosing where delays or packet loss are occurring, and determining whether a routing issue is within the local network, the ISP, or further along the internet path.
  - utility in Windows combines the features of ping and tracert

**pathping**

  - • Traces the path to the destination
  - • Measures latency and packet loss used to verify file system integrity and fix

**chkdsk**

  - logical file system errors
  - • Attempts to recover any readable data

**chkdsk /r              from bad sectors**

  - • Identifies bad sectors on the disk initializes a drive by setting it up with a

**format**

  - structure that supports file storage launches a text-based, command-line

**diskpart**

  - partitioning utility

**md /mkdir              used to create a directory or subdirectory**


**rd / rmdir             used to delete a directory**

  - copying utility which offers the widest range of options
  - • copy an entire folder tree, including all

**robocopy               subdirectories and empty folders**

  - • resume automatically if interrupted due to network issues
  - • copy a very large volume of files displays the name of the current computer a

**hostname**

  - user is connected to lists all local user accounts configured on

**net user**

  - that specific computer

**net user [user name]   View specific user details**

  - launches a pop-up window containing a

**winver                 brief summary of the installed operating**

  - system provides information about the currently

**whoami**

  - logged-on Windows user

**[command name] /?     displaying help or usage information related**


**help [command name]   to a specific utility**

  - refreshes Group Policy settings on a local

**gpupdate              computer without requiring a restart or**

  - logoff used to display current Group Policy settings

**gpresult**

  - for a user or computer concise report of all Group Policy settings

**gpresult /r**

  - that have been applied to a specific host
  - • Replaces incorrect system file versions with correct Microsoft versions

**sfc /scannow**

  - • Scans the integrity of all protected system files moves the command-line prompt one folder
- cd ..
  - up in the directory tree changes the current directory to the root

**cd \**

  - directory (to c: )
  - • verify whether the TCP/IP stack on the local Windows machine is functioning
- ping 127.0.0.1        correctly.
  - • if correct, the issue likely lies further out in the network (e.g., NIC, cable, switch).
  - used for troubleshooting DNS-related

**nslookup**

  - problems map a network share located at

**net use Z:**

  - \\SERVER\Data to the drive letter Z: on a

**\\SERVER\Data**

  - user's computer quickly prepare the D: drive by removing all

**format d: /q          file system references to existing data**

  - without performing a thorough overwrite confirm the network identity of the computer

**hostname**

  - they are currently operating on

**Navigation**


#### 1. cd

  - Displays the name of or changes the current directory cd ..   = backward folder

#### 2. dir

  - Displays a list of files and subdirectories in a directory.

**Network**


#### 1. ipconfig IP configuration

  - Shows your IP address, Subnet Mask, and Default Gateway.
  - : Shows extra details like your MAC address (Physical ipconfig /all
  - Address) and DNS server.
  - ipconfig /release    = Release the IPv4 address for the specified adapter.
  - ipconfig /renew   = Renew the IPv4 address for the specified adapter.

#### 2. ping (Packet InterNet Groper)

  - Sends a small packet to an IP or website and waits for a response
  - Goal: To test connectivity and "latency" (how fast the response is)

#### 3. netstat Network statistics

  - Displays protocol statistics and current TCP/IP network connections.
  - Goal: Used by technicians to find malware "calling home" or to see if a specific port is open

#### 4. nslookup Name server lookup

  - Lookup names and IP addresses

> **Scenario:** You want to know which IP address belongs to
  - microsoft.com

#### 5. net use

  - Connects, disconnects, and displays information about shared resources on the network.

> **Scenario:** Mapping a network folder to a drive letter (e.g., making
  - the company "schematics" folder appear as your h: drive).
  - Example: net use h: \\cheyenne1\schematics

#### 6. tracert Trace Route

  - Shows every "hop" (router) a packet takes to reach a destination
  - Goal: To find exactly which router between you and the destination is failing

#### 7. pathping

  - A hybrid tool that combines ping and tracert
  - It traces the route first, then stays active for several minutes to test each hop for packet loss.
  - Goal: To find intermittent issues or "bottlenecks" where a router is slow but not completely dead.
- Disk management

#### 1. chkdsk

  - Checks a disk and displays a status report.
  - chkdsk /f   = Fixes errors on the disk.
  - chkdsk /r   = Locates bad sectors and recovers readable information

#### 2. format

  - Formats a disk for use with Windows

#### 3. diskpart

  - Manage disk configurations

**File management**


#### 1. md / mkdir

  - Creates a directory

#### 2. rmdir / rd

  - Removes (deletes) a directory

#### 3. robocopy

  - Robust File Copy for Windows
- Feature                copy                robocopy

**Sub-folders            No                  Yes (using /s or /e )**


**Resume on Failure      No                  Yes**


**Mirroring (Syncing)    No                  Yes (using /mir )**


**Speed                  Slow (one by one)   Fast (Multi-threaded)**

  - Full (includes

**File Attributes        Basic**

  - scurity/permissions)

**Informational**


#### 1. hostname

  - View the name of the device

#### 2. net user

  - View All User Accounts
  - View Specific Account Details - net user [username]

#### 3. winver

  - Show Window Version

#### 4. whoami

  - whoami /allThis utility can be used to get user name and group information along with the respective security identifiers (SID), claims, privileges, logon identifier (logon ID) for the current user on the local system

#### 5. [command name] /?

  - check information

**OS management**


#### 1. gpupdate

  - Updates multiple Group Policy settings.

#### 2. gpresult

  - This command line tool displays the Resultant Set of Policy (RSoP) information for a target user and computer.

#### 3. sfc System file check

  - Scans the integrity of all protected system files and replaces incorrect versions with correct Microsoft versions sfc /scannow

### 1.6 Microsoft Windows Control Panel


**Internet Option**


**These settings control how Windows handles network traffic at the**

- system level.

**Device and Printers**


**Function: Add or remove hardware, troubleshoot a printer that isn't**

- working, and see "hidden" devices like wireless dongles.

**Exam Tip: This is the easiest place to set a Default Printer. Look for the**

- green checkmark icon on the printer.

**Program and Feature**


**Function: Uninstall applications, change/repair an installation, or view**

- installed Windows Updates.

**Turn Windows features on or off: This is where you go to**


**enable/disable advanced features like Hyper-V (for virtualization) or**

- the Windows Subsystem for Linux (WSL).

**Network and Sharing Center**


**Function: Shows if you are connected to the internet and what type of**

- network it is (Public vs. Private).

**Change adapter settings: This is the most important link for a**


**technician. It takes you to your Network Connections where you can:**

  - Set a Static IP address.
  - Configure DNS server addresses.
  - Disable/Enable a Wi-Fi or Ethernet card.

**System**


**Shows the CPU type, amount of installed RAM, and the Windows**

- edition/version.

**Advanced System Settings: A critical link for technicians to:**

  - Configure Performance (Visual effects vs. speed).
  - Setup Virtual Memory (Pagefile).
  - Enable Remote Desktop connections.

**Window Defender Firewall**


**Function: It blocks or allows traffic based on rules to protect the PC**

- from hackers or malware.

**Advanced setting**

  - Inbound Rules: Controls traffic coming into the PC.
  - Outbound Rules: Controls traffic going out of the PC.

**Mail**

- Purpose: It allows you to manage Outlook "Profiles," email accounts,

**and data files**


**A+ Scenario: If Outlook is crashing or won't open, a technician often**

- goes here to create a new Profile to see if the old one was corrupted. It is also used to set a password on a local data file.

**Sound**


**Playback Tab: Choose where the sound comes out (e.g., switching**


**from laptop speakers to a HDMI monitor or USB headset)**

- Recording Tab: Configure microphones and set gain levels.

**Exam Tip: This is where you set the "Default Device." If a user says "I**


**can hear my music but my mic doesn't work in Teams," you check the**

- Default Communication Device here.

**User Accounts**

- Purpose: Change your account type (Standard vs. Administrator),

**change your password, or manage your User Account Control (UAC)**

- settings.

**UAC: That pop-up that asks "Do you want to allow this app to make**

- changes?" You can slide the bar here to make it more or less strict.

**Device Manager**

- Purpose: The central spot to manage hardware drivers.

**Symbols to Know:**

  - Yellow Exclamation (!): Driver is missing or corrupted.
  - Red X or Down Arrow: The device is manually disabled.

**Action: You can Update, Roll Back (go back to a previous version), or**

- Uninstall drivers here.

**Indexing Options**


**Purpose: Windows builds an "index" (a catalog) of your files so that**

- when you search in the Start menu, the results appear instantly.

> **Scenario:** If a user says "I know the file is in my folder, but Windows

**Search can't find it," you come here to Rebuild the Index. You can also**

- choose which folders Windows should or should not look into.

**Administrative Tools （Windows tools)**

- Contents: It holds shortcuts to Computer Management, Event Viewer,
- Services, Performance Monitor, and Task Scheduler.

**This is the "One-Stop Shop" for a technician. If you don't remember the**

- specific command, you just go here to find the icon.

**File Explorer Options**


#### 1. View hidden files

  - To find logs, AppData, and hidden malware.

#### 2. Hide extensions

  - To identify dangerous executable files disguised as documents.

#### 3. General options

  - Choose if every folder opens in a new window or the same window.

#### 4. View options

- Power Options

#### 1. Hibernate

  - Windows takes everything in your RAM and writes it to a file on your disk

#### 2. Power plans

  - Balanced: The default. It automatically increases CPU speed when needed and lowers it when the PC is idle.
  - Power Saver: Limits CPU performance and lowers screen brightness to maximize battery life.
  - High Performance: Keeps the CPU at higher speeds constantly.
  - This uses more power and creates more heat but is better for tasks like video editing or gaming.

#### 3. Sleep/suspend

  - The computer stays "on" just enough to keep your open apps in the
  - RAM. If the battery dies, you lose your unsaved work.

#### 4. Standby

  - Instant-on for a meeting

#### 5. Choose what closing the lid does

  - You can configure the laptop to Do Nothing, Sleep, Hibernate, or
  - Shut Down when the lid is closed

#### 6. Turn on fast startup

  - This is a hybrid of Shutdown and Hibernate

**Ease of Access**


**Making the PC usable for everyone**

- Change display, keyboard, mouse, and other input/output options

**Time and Language**


**Setting the timezone**

- Changing the local currency and date formats

**Update and Security**

- Windows Update: Checking for security patches and feature updates.

**Windows Security: The interface for Windows Defender (Antivirus**

- and Firewall).

**Recovery: Accessing "Reset this PC" or "Advanced Startup" (to get**

- into Safe Mode).

**Personalization**

- Background & Colors: Changing wallpapers and Dark/Light mode.
- Lock Screen: Choosing which apps show info while the PC is locked.

**Taskbar: Hiding the taskbar or changing icon alignment (Left vs. Center**

- in Win 11).

**Apps**


**Apps & Features: The modern version of "Programs and Features."**

- Used to uninstall apps.

**Default Apps: Choosing which browser opens links (e.g., changing**

- from Edge to Chrome).

**Startup: Managing which apps launch at login (mirrors the Task**

- Manager Startup tab).

**Privacy**

- App Permissions: Controlling which apps can access your Camera,
- Microphone, and Location.
- General: Managing your "Advertising ID" and tracking.

**System**

- Display: Resolution, scaling, and multiple monitor setup.

**Sound: Choosing input/output devices (mirrors the Control Panel**

- "Sound" applet).
- Notifications: Managing "Focus Assist" to block pop-ups.

**Storage: Accessing Storage Sense, which automatically clears**

- temporary files.

**About: Shows the Device Name, Processor, RAM, and Windows**

- Version (Home/Pro).

**Bluetooth & Devices**


**Manage devices**


**Mouse settings**

- Typing and writing

**Network and Internet**

- Status: Shows if you are connected to the web.
- Wi-Fi/Ethernet: Managing known networks and hardware properties.
- Proxy/VPN: Configuring corporate connection settings.
- Data Usage: Seeing which apps are using the most bandwidth

**Gaming**

- Game Bar: Overlay for recording clips.
- Game Mode: Prioritizes system resources for the game process

**Accounts**


**Your Info: Checking if you are using a Local Account or a Microsoft**

- Account.

**Sign-in Options: Configuring Windows Hello (Fingerprint, Face ID, or**

- PIN).
- Family & Other Users: Where you go to add a new person to the PC

### 1.7 Microsoft Windows networking


**Domain joined vs. workgroup**


#### 1. Shared resources

  - Workgroup: A Workgroup is a decentralized network where every computer is an equal (a "peer")
  - Domain: A Domain is a centralized network managed by at least one server called a Domain Controller (DC)

#### 2. Printers

  - Workgroup: Each user must manually install the driver for the shared printer.
  - Domain: Printers are "published" in Active Directory. Users can simply search the directory for "Floor 2 Printer" and it installs automatically.

#### 3. File Servers

  - Workgroup: Usually just a regular PC that stays on all the time.
  - Access is managed by local user permissions.
  - Domain: A dedicated server (Windows Server). Access is managed through Security Groups in Active Directory. If you are in the
  - "Marketing" group, the server automatically knows you have access to the Marketing folder.

#### 4. Mapped drives

  - Workgroup: You must manually map the drive on each PC using the net use command or File Explorer. If the host PC’s password changes, the map breaks.
  - Domain: Administrators use Group Policy Scripts to automatically map drives (e.g., the S: drive) for every user the moment they log in.
  - use command tool to map drive. net use \\server\folder
- Local OS firewall settings

#### 1. Configuration

  - Control panel > Windows Defender Firewall with Advanced Security
  - Inbound Rules: These protect your PC from the outside world. They block or allow traffic trying to enter your computer (e.g., someone trying to Remote Desktop into your PC).
  - Outbound Rules: These control traffic leaving your computer.
  - Technicians use these to stop malware from "calling home" to a hacker's server.
  - Connection Security Rules: Used for setting up IPsec (Internet
  - Protocol Security) to encrypt data moving between specific computers.

#### 2. Application Restrictions and Exceptions


**Client network configuration**


#### 1. Internet Protocol (IP) addressing scheme

  - PC need IP to access internet. such as you need an “phone number” to contact others

#### 2. Domain Name System (DNS) settings

  - Domain Name System (DNS) protocol is the protocol used to provide names for an IP address based on their mappings in a database using TCP/UDP port 53.

#### 3. Subnet mask

  - The subnet mask is used to identify the host identifier and the network identifier uniquely in combination with the IP address.

#### 4. Gateway (Router IP address)

  - The default gateway parameter is the IP address of a router to which packets destined for a remote network should be sent by default.

#### 5. Static vs. dynamic

  - Dynamic- DHCP (Automatic IP addressing)
  - Static - Assign IP address manually

**Establish network connections**


#### 1. Virtual private network (VPN)

  - A VPN creates an encrypted "tunnel" over a public network (like the
  - Internet) to safely connect a client to a private corporate network.

#### 2. Wireless

  - Uses radio waves (802.11 standards) to connect to a Wireless
  - Access Point (WAP).
  - Configuration:
  - 1. Select the SSID (Service Set Identifier/Network Name).
  - 2. Enter the Security Key (WPA2/WPA3).
  - If a hidden SSID is used, you must manually type in the name and security type in "Network and Sharing Center.”

#### 3. Wired (Ethernet)

  - The most stable and fastest connection type, typically using an RJ-
  - 45 connector.
  - Configuration: Usually "Plug and Play." Once the Cat5e or Cat6 cable is plugged into the NIC (Network Interface Card) and a switch/router, the OS automatically negotiates the speed.
  - Troubleshooting: Look for the "link lights" on the NIC.
  - Solid Green: Connected.
  - Flashing Amber: Activity/Data transfer.
  - No light: Physical layer failure (bad cable or port).

#### 4. Wireless wide area network (WWAN)/cellular network

  - Wireless Wide Area Network connections use cellular towers (4G
  - LTE/5G) to provide internet to laptops or tablets.
  - Hardware Requirements: A built-in cellular modem or an external
  - USB "dongle."
  - SIM Card: Just like a phone, these devices require a SIM card for authentication with the carrier (e.g., Maxis, Celcom, or Digi in
  - Malaysia).
  - Usage: Managed in Windows under Settings > Network & Internet
  - > Cellular

**Proxy settings**


**A Proxy Server acts as an intermediary. Instead of your computer**


**talking directly to a website, it sends the request to the Proxy, which**

- fetches the data for you.
- Configuration: Found in Settings > Network & Internet > Proxy.

**Windows Control Panel (category view) > Network and Internet >**


**Internet Options > Connections tab > LAN settings > Proxy server**


**function:**

  - Monitoring of accessed content by clients
  - Enables the use of content filtering
  - Provides caching of accessed pages

**Public network vs. private network**


#### 1. Private

  - Share and connect to devices
  - Home or work network

#### 2. Public

  - No sharing or connectivity
  - Public Wi-Fi
- File Explorer navigation–network paths

**The Format: \\ServerName\SharedFolderName**


**Mapping: If you use a path frequently, you "Map" it to a drive letter (like**

- the S: drive) so it shows up in "This PC."

**Metered connections and limitations**


**A metered connection is a setting you toggle when you have a limited data**

- plan (common with WWAN/Cellular or mobile hotspots).

**What Windows Does:**

  - Pauses Windows Updates: Only critical security patches are downloaded.
  - Restricts Background Data: Apps won't sync in the background
  - (e.g., OneDrive pauses syncing).
  - Live Tiles: Stop updating to save data.

**Technician Tip: If a user complains that "Windows Update isn't**

- working" or "My files aren't syncing to the cloud," check if their Wi-Fi is accidentally set to Metered.

### 1.8 MacOS/desktop operating system


**Installation and uninstallation of applications**


**File type**


**.pkg (Installer Package) - files are compressed files used to install a**


**macOS application**


**.dmg (Disk Image) - It stands for "Disk Image." When you double-**


**click it, macOS "mounts" it as if you just plugged in an external drive**

- or inserted a disc.

**.app - files are installed applications. Must have an apple ID to setup**

- and download apps
- Apps Store
  - macOS includes an App Store which includes free and paid applications
  - Application can be downloaded and installed from a vendor's website, but it is NOT enabled by default

**Uninstallation Process**

  - Simply dragging the .app file to the Trash installed via the App Store can be deleted from Launchpad lled through .pkg files may require a dedicated uninstaller

**System folders**

- /Applications - the default location for both Apple-supplied and user-

**installed software**


**/Users/[username] - access personal files in macOS**


**/Library - macOS folder containing system-wide resources and settings**


**/System - the core OS files necessary for the system to run**


**/Users/[username]/Library - macOS folder designed to store application**

- data and settings specific to an individual user account

**Apple ID and corporate restrictions**


**Apple ID - With SSO (Single Sign-on), access exclusive to Apple’s own**


**ecosystem of products and services**


**Corporate restrictions - MDM (Mobile Device Management) uses a**


**built-in framework in macOS that allows an organization to manage**

- devices remotely and wirelessly
- Best practices

**Backups**

  - As often as data is changing or as must as you are will to lose
  - Time Machine (Local) + iCloud/Offsite (Cloud).

**Antivirus**

  - Should have 3rd party antivirus installed
  - Keep Gatekeeper strict and ensure XProtect is active.

**Updates/patches**

  - Install updates as apple releases them

**Rapid Security Response (RSR)**

  - Apple-exclusive mechanism for deploying time-sensitive security patches independently of major OS updates
- System Preferences

**Display**

- Configure display setting such as resolution or multiple monitors

**Network**

- Set network configuration

**Printer**

- Add, manage or remove printers

**Scanners**

- Add, manage or remove Scanners

**Privacy**

- Manage privacy settings

**Accessibility**

  - Configure the system for people with disabilities

**Time Machine**

  - Backup mechanism of macOS

**Features**


**Multiple desktops**

  - Use Mission Control to create additional desktops, called spaces, to organize the windows
- Mission Control
- View and manage all open application windows

**Keychain**


**Stores your passwords and account information, and reduces the**

- number of passwords you have to remember and manage.

**Spotlight**

- Finds items on your Mac, like apps, files, and emails

**iCloud**


**Backup and synchronize your photos, files, backups, and more**


**across all your devices**


**iMessage - Send/receive texts (SMS and iMessage) from your**

- laptop.

**FaceTime - Real-time audio and video calling between Apple**


**devices**

- iCloud Drive - stores files in cloud and access from any device

**Gestures**


**Apple trackpad or a Magic Mouse with your Mac, you can use**

- gestures.

**Finder**

- default file management application for macOS

**Dock**


**similarly to the Windows taskbar, providing quick access to**


**frequently used and running applications, as well as minimized**

- windows

**Continuity**


**allowing users to seamlessly transition tasks and data between**

- different Apple devices
- Disk Utility
- Can be used to partition and initialize storage devices.

**It also is used to access First Aid which can repair permissions and recover**

- corrupted files.
- macOS tool allows users to create .dmg files
- FileVault

**Disk encryption program**


**Encrypts the contents of the startup disk to protect user data from**

- unauthorized access
- Terminal

**Unix command line for MacOs**

- macOS tool provides access to different command-line shells
- Force Quit

**Terminate an unresponsive application or process**

- Choose Force Quit from the Apple menu in the corner of your screen

### 1.9 Linux feature and command


> 💡 **Key Tip:** for assist or help: use [command] --help or man [command]


**File management**


#### 1. Finding Where You Are


**pwd   (Print Working Directory)**

  - What it does: It tells you exactly which folder you are currently standing in.
  - Analogy: The "You are here" dot on a mall map.

**ls    (List)**

  - What it does: Shows you all the files and folders inside your current directory.
  - Technician Tip: Use ls -l (the long list) to see file sizes and permissions, or ls -a to see "hidden" files that start with a dot (.).

#### 2. Moving and Copying


**cp   (Copy)**

  - What it does: Makes a duplicate of a file or folder.
  - Syntax: cp [source] [destination]

**mv   (Move / Rename)**

  - What it does: Moves a file from one place to another. In Linux, there is no "Rename" command; you just "move" a file to a new name.
  - Syntax: mv old_name.txt new_name.txt

#### 3. Deleting


**rm   (Remove)**

  - What it does: Deletes a file.
  - Warning: There is no "Recycle Bin" in the Linux terminal. Once you rm a file, it is gone forever.
  - Technician Tip: To delete a folder and everything inside it, use rm - r (recursive).

#### 4. Searching


**grep    (Global Regular Expression Print)**

  - What it does: Searches for specific text inside a file.
  - Example: If you have a massive log file and only want to find errors, you use grep "error" logfile.txt .

**find    (Find)**

  - What it does: Searches for files and folders by name, size, or date.
  - Example: find . -name "*.jpg" (Find every JPG in the current folder).

#### 5. Permissions & Ownership (The "Security" Commands)


**This is a high-priority topic for the exam. Linux handles security using a**

- "User-Group-Others" system.
- chmod   (Change Mode)
  - What it does: Changes the permissions of a file (who can Read [4],
  - Write [2], or Execute [1] it). = rwx[7]
  - Example: chmod 777 gives everyone full control. (Don't do this in a real job!)

**chown   (Change Owner)**

  - What it does: Changes which user or group owns the file.
  - Analogy: Handing the keys of a house from one person to another.

**Filesystem management**

- mount
  - What it does: It tells the Linux OS to connect a physical storage device (like a USB drive or a second SSD) to a specific folder so you can see the files.
  - The Workflow: If you plug in a drive, it might be named /dev/sdb1 .
  - You "mount" it to a folder like /mnt/usb , and suddenly your files appear in that folder.

**fsck    (File System Consistency Check)**

  - What it does: This is the Linux version of chkdsk in Windows. It scans the hard drive for errors and tries to repair them.
  - Technician Tip: You usually run this if a system was shut down improperly or if you see "File System Read-Only" errors.

**Package management**


**apt    (Advanced Package Tool)**

  - Family: Debian and Ubuntu.
  - Common Commands:
  - sudo apt update   (Refresh the list of available software).
  - sudo apt install [app]   (Download and install).

**dnf    (Dandified YUM)**

  - Family: Red Hat, Fedora, and CentOS.
  - Common Commands:
  - sudo dnf upgrade   (Update all system software).
  - sudo dnf install [app]   .

**Administrative Commands**


**su   (Substitute User)**

  - What it does: It allows you to switch completely to another user account (usually the Root account, which is the "God mode" account).
  - Usage: You type su - , enter the root password, and now every command you type is as the administrator until you log out.

**sudo   (SuperUser Do)**

  - What it does: This is the most common way to run administrative tasks. It allows you to run a single command with root privileges.
  - Analogy: It’s like the Windows "Run as Administrator" right-click option.
  - A+ Note: It is much safer than su because it logs who did what and only grants power for that one specific task.

**Network**


#### 1. ip (IP Address Management)


**What it does: It shows or configures the network interfaces on your**

- Linux machine (IP address, status, and subnet mask).
- The Command: Most technicians use ip address (or ip addr ).

**A+ Tip: In the old days, Linux used ifconfig . While you might still see**

- ifconfig on older systems, the current standard for the exam is the ip command.
- Windows Equivalent: ipconfig .

#### 2. ping (Connectivity Test)


**What it does: It sends a small packet of data to another IP address or**

- website and waits for a response.

**Why use it: To see if a device is "alive" and how long it takes to talk**

- back (latency).

**Linux Difference: On Windows, ping stops after 4 tries. On Linux, it will**

- ping forever until you stop it by pressing Ctrl + C.

#### 3. traceroute (Path Tracking)


**What it does: It shows the path a packet takes to reach a destination. It**

- lists every "hop" (router) the data passes through.

**Why use it: If you can't reach a server, traceroute tells you exactly**

- which router along the way is failing.
- Windows Equivalent: tracert .

#### 4. dig (Domain Information Groper)


**What it does: It queries DNS servers to look up the IP address of a**

- domain name (like google.com ).

**Why use it: If you think your DNS is broken or a website is pointing to**


**the wrong IP, dig will show you exactly what the DNS server is**

- reporting.
- Windows Equivalent: nslookup .

#### 5. curl (Client URL)


**What it does: It is a tool for transferring data to or from a server. In its**


**simplest form, it "downloads" the content of a webpage or a file directly**

- into your terminal.

**Why use it: Technicians use it to see if a web server is responding**

- correctly without needing to open a browser.

**Example: curl [http://www.google.com](http://www.google.com) will show you**

- the raw HTML code of Google's homepage.
- Informational

**Getting Help**


**man   (Manual)**

  - What it does: This is the built-in instruction manual for almost every command in Linux.
  - How to use: Type man followed by the command name (e.g., man ls ). It opens a text page explaining all the "switches" (options) for that command.
  - To exit: Press q .

#### 2. Viewing File Content


**cat   (Concatenate)**

  - What it does: It displays the entire content of a text file right in your terminal window.
  - Why use it: It’s the fastest way to read a log file or a configuration file without opening an editor.
  - Technician Tip: If the file is very long, it will scroll past your eyes instantly. (For long files, professionals often use more or less instead).

#### 3. Monitoring Processes (CPU/RAM)


**ps    (Process Status)**

  - What it does: It takes a "snapshot" of the programs currently running.
  - Common Use: ps -ef or ps aux shows every process running on the system, including who started it and its PID (Process ID).

**top   (Table of Processes)**

  - What it does: This is the Linux version of Task Manager. It shows a real-time, live-updating list of processes.
  - Why use it: To see which app is "hogging" the CPU or RAM.
  - Windows Equivalent: Task Manager (Processes tab).

#### 4. Checking Storage Space


**df   (Disk Free)**

  - What it does: Shows you how much space is left on your entire hard drive or partitions.
  - Technician Tip: Use df -h (the h stands for "human-readable").
  - Instead of showing bytes, it will show GB and MB.

**du   (Disk Usage)**

  - What it does: Shows the size of a specific file or folder.
  - Why use it: If df tells you the disk is full, you use du to hunt down exactly which folder is taking up all that space.

**Text Editor**

- nano

**Unlike the more complex vi , nano is designed to be simple and user-**

- friendly for beginners and technicians.
- How to use: Type nano filename.txt .
- The Interface: The bottom of the screen shows a menu of commands.
- The ^ symbol stands for the Ctrl key.
  - Ctrl + O: "Write Out" (Save the file).
  - Ctrl + X: Exit the editor.
  - Ctrl + W: "Where Is" (Search for a word).

**Common configuration files**


**/etc/passwd (User Information)**

- What it is: A list of every user account on the system.

**What it contains: Username, User ID (UID), Group ID (GID), their home**

- directory path, and which "Shell" they use (like /bin/bash ).

**Technician Tip: It does not contain the actual passwords anymore for**

- security reasons.

**/etc/shadow (Secure Passwords)**


**What it is: The highly protected file that actually stores the encrypted**

- passwords.

**Security: Only the Root user (administrator) can read this file. It uses**

- salted hashes to keep passwords safe even if someone steals the file.

**/etc/hosts (Local Name Resolution)**


**What it is: A local list of IP addresses and the hostnames they belong**

- to.

**How it's used: Before your computer asks a DNS server (like Google's**

- 8.8.8.8) where a website is, it checks this file first.

**Technician Tip: You can use this to block websites or map a server IP to**

- a nickname for easy access.

**/etc/fstab (File System Table)**

- What it is: The "to-do list" for the mount command.

**What it does: It tells Linux which hard drives and partitions should be**

- mounted automatically every time the computer boots up.
- A+ Scenario: If you add a new permanent hard drive to a Linux server, you must add a line to this file so it stays connected after a restart.

**/etc/resolv.conf (DNS Resolver)**

- What it is: This file tells Linux which DNS Servers to use.
- What it contains: Usually a line that says nameserver 8.8.8.8 .

**A+ Scenario: If you can ping an IP address but cannot open a website**

- by name, this is the first file you check to see if the DNS IP is correct.

**OS components**


#### 1. The Kernel

- The Kernel is the absolute core of the operating system.

**What it does: It is the "Master Translator." It sits between the hardware**


**(CPU, RAM, Disk) and the software. If a program wants to use memory**

- or talk to the network, it must ask the Kernel.

**Key Fact: The Kernel is loaded into memory during boot and stays there**

- until the system shuts down.

**Technician Tip: When you hear about a "Kernel Panic" in Linux or**


**macOS, it means the Kernel encountered a critical error it couldn't**

- recover from (the equivalent of a Windows Blue Screen).

#### 2. The Bootloader

- The Bootloader is the "Starter Motor" for the computer.

**What it does: It is the first piece of software that runs. Its only job is to**

- find the Kernel on the hard drive, load it into RAM, and start it.
- Most Common Version: GRUB (Grand Unified Bootloader).
- A+ Scenario: If the bootloader is corrupted, the hardware will turn on,

**but the OS will never start. You’ll see a "Boot device not found" or a**

- grub> prompt.

#### 3. systemd

- Once the Kernel is loaded, it starts systemd.

**What it does: It is the "Manager of Managers." It is the first process to**


**start (it has PID 1) and it is responsible for starting all other services (like**

- the network, the GUI login screen, and print services).

**Modern Standard: Almost all major Linux versions (Ubuntu, Fedora, Red**

- Hat) now use systemd .

**Technician Tool: You use the command systemctl to talk to systemd**

- (e.g., sudo systemctl restart network ).

**Root Account**

- In Linux, the Root Account is the "Superuser" or "God Mode" account.

**Power: The Root account can do anything—including deleting the entire**

- operating system with a single command. It ignores all file permissions.

**Security Best Practice:**

- Never log in as Root for daily tasks.
- Use sudo to borrow Root's power only when necessary.

**The Symbol: In the terminal, if your prompt ends in a $ , you are a**

- standard user. If it ends in a # , you are logged in as Root.

### 1.10 Install applications according to requirements

- System requirements for applications

> 💡 **Key Tip:** Before installing software, check if the computer meets minimum requirements.


**32-bit vs 64-bit application requirements**

- This is heavily tested.

**32-bit**

- Older architecture.

**Limits:**


**Max around 4GB RAM usable**

- Older apps/drivers

**64-bit**

- Modern architecture.

**Benefits:**


**Supports more RAM**


**Better performance**

- Required by many modern apps

**Rules**


**64-bit OS can run 32-bit apps ✅ usually yes**

- 32-bit OS cannot run 64-bit apps ❌
- This is important.

**Scenario**


**A user downloads a 64-bit accounting program, but installation fails on**

- their PC running 32-bit Windows.

**Cause?**

- ✅ OS architecture incompatibility

> **Answer:** 

**32-bit OS cannot run 64-bit application**


**Dedicated vs Integrated Graphics Card**

- Graphics processing.

**Integrated graphics**

- Built into CPU/motherboard.

**Examples:**


**Office work**


**Browsing**

- Video playback
- Uses shared system RAM.
- Cheaper.

**Dedicated graphics card (GPU)**

- Separate graphics hardware.
- Examples:

**Gaming**


**3D rendering**


**Video editing**

- CAD
- Has own VRAM.
- More powerful.

**Scenario**


**User installs 3D design software, but app says:**

- Dedicated GPU required.
- Their laptop only has Intel integrated graphics.

**Issue?**

- ✅ Hardware requirement not met

> **Think:** 

**Integrated = basic**


**Dedicated = heavy graphics work**


**VRAM Requirements**


**VRAM = Video RAM**

- Memory specifically for graphics.

**Used for:**


**textures**


**rendering**

- video processing

**Example requirements:**

- 2GB VRAM minimum
- 8GB recommended

**Scenario**

- Video editing app requires 4GB VRAM, GPU only has 2GB.

**Issue?**

- ✅ Insufficient VRAM

**Memory:**


**RAM = system memory**


**VRAM = graphics memory**


**RAM Requirements**

- Application needs enough memory.

**Examples:**


**8GB minimum**

- 16GB recommended

**Low RAM symptoms:**


**slow**


**freezing**

- crashes

**Scenario**


**User installs VM software on 4GB RAM laptop and system becomes**

- unusable.

**Cause?**

- ✅ insufficient RAM

**CPU Requirements**

- Processor must meet requirements.
- Check:

**speed (GHz)**


**architecture**

- cores

**Example:**


**Intel i5 minimum**

- 4 cores required

**Scenario**

- Software requires AVX-supported CPU but PC has older processor.

**Issue?**

- ✅ CPU incompatibility

**External Hardware Tokens**

- Physical security devices needed.

**Examples:**


**USB dongle**


**smart card**

- hardware key

**Common in:**


**licensed software**

- MFA authentication

**Scenario**


**Software installs successfully but cannot launch without USB license**

- key.

**Requirement?**

- ✅ External hardware token
- Storage Requirements
- Need enough disk space.

**Examples:**

  - 20GB free storage

**Check:**

  - install size temp files updates

**Scenario**

- Install fails because disk only has 2GB free, app needs 10GB.

**Issue?**

- ✅ insufficient storage

**Application to OS Compatibility**

- App must support OS version.

**Examples:**

  - Windows 11 only macOS version requirement
  - Linux dependency

**Scenario**

- App supports Windows 11 but user runs Windows 8.

**Issue?**

- ✅ OS compatibility problem
- Distribution methods

> 💡 **Key Tip:** How software is installed.


**Physical Media**

- Traditional installation media.

**Examples:**


**DVD**

- USB installer

> **Scenario:** 
- Company installs software from DVD.

**Method?**

- ✅ Physical media

**Mountable ISO File**

- ISO = disk image file.
- Can mount like virtual DVD.

**Common for:**


**OS installs**

- software packages

**Example:**

- Double click ISO → appears as DVD drive.

**Scenario**

- Technician downloads Windows installer ISO and mounts it.

**Method?**

- ✅ Mountable ISO

**Downloadable Package**

- Install from internet.

**Examples:**

- .exe
  - .msi
  - .pkg
  - .deb
- Most common today.

> **Scenario:** 
- User downloads Chrome installer.

**Method?**

- ✅ Downloadable package

**Image Deployment**

- Deploy preconfigured system/software image.
- Used in enterprises.

**Example:**

- Deploy same Windows image to 100 PCs.

**Benefits:**

  - faster standardized

> **Scenario:** 
- School installs same software setup on all lab computers automatically.

**Method?**

- ✅ Image deployment

> **Think:** 
- One image → many devices
- Impact considerations for new applications

> 💡 **Key Tip:** Installing software affects more than one computer.


**Device impact**

- How software affects machine.

**Questions:**


**enough RAM?**


**CPU load?**

- battery drain?

> **Scenario:** 
- New antivirus slows older PCs.

**Impact?**

- ✅ Device impact

**Network impact**

- Software affects network.

**Examples:**


**cloud sync traffic**


**updates**

- bandwidth use

> **Scenario:** 
- New backup software consumes bandwidth every hour.

**Impact?**

- ✅ Network impact

**Operation impact**

- Affects workflow/process.

**Examples:**


**downtime**


**training**

- compatibility

> **Scenario:** 
- New POS software requires employee retraining.

**Impact?**

- ✅ Operational impact

**Business impact**

- Big picture business effects.

**Examples:**

  - cost productivity compliance revenue

> **Scenario:** 
- Accounting software migration causes billing delays.

**Impact?**

- ✅ Business impact

> **Think:** 
- Business = money/process consequences

### 1.11 cloud productivity tools


**Email Systems**

- Cloud email hosted online instead of local mail server.

**Examples:**


**Microsoft Outlook**

- Gmail
- Functions:
  - Send/receive email
  - Calendar
  - Contacts
  - Shared mailboxes

**Common IT tasks**

  - Create mailbox
  - Reset password
  - Configure client access
  - Assign email license

**Scenario**

- A new employee cannot access company email after account creation.

**Most likely issue?**

- ✅ License not assigned

**or**

- ✅ Mailbox not provisioned

**Another scenario:**

- User changed password but phone mail app still fails.

**Fix?**

- ✅ Update stored credentials

**Storage**

- Cloud storage = files stored online.

**Examples:**

  - OneDrive
  - Google Drive
- Dropbox

**Benefits:**


**backup**


**sharing**


**access anywhere**

- sync devices

**Sync/folder settings**

- Very testable.
- Sync = keep local and cloud files matching.
- You choose which folders sync.

**Examples:**


**Desktop sync**


**Documents sync**

- selective sync

**Scenario**

- User’s laptop storage is full after syncing all cloud folders.

**Fix?**

- ✅ Change sync/folder settings

**or selective sync**

- Because not all files should download locally.

**Another scenario:**

- User saved file in cloud but cannot see it on desktop.

**Cause?**

- ✅ sync disabled

**Memory:**

- Sync issue = check sync settings first.
- Collaboration Tools

> 💡 **Key Tip:** Multiple users work together online.


**Spreadsheets**

- Cloud spreadsheets.

**Examples:**

  - Microsoft Excel
  - Google Sheets

**Features:**

  - shared editing formulas comments
  - Scenario
- Two employees edit same budget file simultaneously.

**Tool?**

- ✅  Spreadsheet collaboration

**Videoconferencing**

- Remote meetings.

**Examples:**

  - Microsoft Teams
  - Zoom
  - Google Meet
- Features:

**video meetings**


**screen sharing**

- chat

**Scenario**

- Remote team needs weekly meetings with screen sharing.

**Tool?**

- ✅ Videoconferencing

**Presentation Tools**

- Create slides.

**Examples:**


**Microsoft PowerPoint**

- Google Slides

> **Scenario:** 
- Marketing team creates shared product presentation.

**Tool?**

- ✅ Presentation tools

**Word Processing Tools**

- Documents/text editing.

**Examples:**


**Microsoft Word**

- Google Docs

**Features:**


**documents**


**comments**

- track changes

> **Scenario:** 
- HR team edits policy handbook together.

**Tool?**

- ✅ Word processing

**Instant Messaging**

- Real-time chat.

**Examples:**

  - Slack
  - Microsoft Teams

**Features:**

  - chat channels file sharing

> **Scenario:** 
- Employees need quick communication without email.

**Tool?**

- ✅ Instant messaging

**Identity Synchronization**

- This is slightly more admin-related.

**Meaning:**

- Sync user identities/accounts between systems.

**Examples:**


**On-prem Active Directory sync to cloud**

- Same username/password across cloud apps

**Benefits:**

- one login centralized management

**Often called:**


**directory sync**

- identity sync

**Scenario**

- Employee password changed locally but cloud login still uses old password.

**Problem?**

- ❌ identity synchronization issue

**Another:**

- User created in local AD but not appearing in cloud tenant.

**Issue?**

- ✅ sync failure

> **Think:** 

**Identity sync = account info sync**


**Licensing Assignment**

- Users need proper licenses to access cloud apps.
- Very common exam question.

**Without license:**


**no email**


**no Teams**


**no OneDrive**

- no Office apps

**Scenario**

- New employee account exists but cannot use Outlook or Teams.

**First check?**

- ✅ Licensing assignment

**Another:**

- Manager needs spreadsheet app but only basic email enabled.

**Fix?**

- ✅ assign proper license

> **Think:** 
- No access after account creation = check license.

---

## 2.0 Security


### 2.1 Security Control+

- Physical security

> 💡 **Key Tip:** How do you physically stop unauthorized people from accessing buildings, rooms, or equipment?


**Bollards**


**Meaning:**

- Strong vertical posts/barriers placed outside buildings.

**Purpose:**

  - stop vehicles prevent car ramming attack protect entrance

**Usually outside:**

  - office buildings

**banks**

- government buildings

**Scenario**


**Company wants to prevent vehicles from crashing into building**

- entrance.

> **Answer:** 
- ✅ Bollards

**Looks like:**

- short metal/concrete posts.

**Memory:**

- Bollards = anti-car poles.

**Access Control Vestibule**


**Also called:**


**mantrap**

- Very testable.

**Meaning:**

- Small enclosed area with controlled doors.
- Process:

#### 1. Enter first door


#### 2. Authenticate


#### 3. Second door opens


**Prevents:**


**tailgating**

- unauthorized access

**Scenario**

- Only one person allowed through secured entrance at a time.

> **Answer:** 
- ✅ Access control vestibule

**Used in:**


**data centers**

- secure offices

**Memory:**

- Security airlock for humans.

**Badge Reader**

- Reads employee access badges/cards.

**Examples:**


**RFID card**


**swipe card**

- proximity card

**Purpose:**


**authenticate building access**

- track entry

**Scenario**

- Employees tap ID card to unlock office door.

> **Answer:** 
- ✅ Badge reader

**Benefits:**


**logging access**

- controlled entry

**Memory:**


**Tap card = badge reader**


**Video Surveillance**

- Security cameras.

**Purpose:**


**monitor activity**


**record evidence**

- deter crime

**Examples:**

- CCTV

**Scenario**

- Company wants to monitor server room activity.

> **Answer:** 
- ✅ Video surveillance

**Benefits:**


**evidence collection**

- incident review

**Memory:**

- Security cameras.
- Alarm Systems
- System alerts when security event occurs.

**Triggers:**


**unauthorized entry**


**broken window**

- forced door

**Purpose:**

- alert staff/security

**Scenario**

- Building should alert staff when break-in detected after hours.

> **Answer:** 
- ✅ Alarm system

**Types:**


**burglar alarm**

- fire alarm

**Memory:**

- Intrusion alert.

**Motion Sensors**

- Detect movement.

**Often connected to:**


**alarm systems**


**lights**

- cameras

**Purpose:**

- detect unauthorized movement

**Scenario**

- Server room should detect movement after business hours.

> **Answer:** 
- ✅ Motion sensors

**Common technologies:**

- infrared

**Memory:**

- Movement detector.

**Door Locks**

- Basic physical security.

**Types:**


**key locks**


**electronic locks**

- smart locks

**Purpose:**

- prevent unauthorized entry

**Scenario**

- Office wants to secure storage room.

> **Answer:** 
- ✅ Door locks
- Simple but essential.

**Memory:**

- Classic access control.
- Equipment Locks
- Locks devices physically.

**Examples:**


**laptop lock**


**server rack lock**

- cable lock

**Purpose:**

- prevent theft/removal

**Scenario**

- Company wants to secure laptops in public workspace.

> **Answer:** 
- ✅ Equipment locks

**Example:**

- Kensington lock.

**Memory:**

- Lock hardware itself.

**Security Guards**

- Human physical protection.

**Purpose:**


**monitor area**


**verify visitors**

- respond incidents

**Benefits:**


**human judgment**

- deterrence

**Scenario**

- Building requires personnel to verify visitor identity.

> **Answer:** 
- ✅ Security guards

**Useful for:**


**access enforcement**

- incident response

**Memory:**

- Human security layer.

**Fences**

- Perimeter security barrier.

**Purpose:**


**restrict area access**


**delay intruders**

- define boundaries

**Used around:**


**offices**


**warehouses**

- data centers

**Scenario**

- Company wants to restrict physical access to property perimeter.

> **Answer:** 
- ✅ Fences

**Memory:**

- Outer barrier.
- Physical access security

> 💡 **Key Tip:** How people prove identity to enter a building, room, or device.


**Key Fobs**

- Small electronic device used for access.

**Often:**

  - RFID proximity device
- User taps or brings close to reader.

**Examples:**

  - office door access token apartment access tag

**Scenario**

- Employee taps small device on door reader to unlock entrance.

> **Answer:** 
- ✅ Key fob

**Benefits:**


**easy access**

- can deactivate if lost

**Memory:**

- Small keychain access device.

**Smart Cards**

- Card with embedded chip.

**Can store:**


**credentials**


**certificates**

- access data
- Often inserted or tapped.

**Examples:**


**employee ID smart card**

- government card

**Scenario**

- Employee inserts chip-enabled card into reader for authentication.

> **Answer:** 
- ✅ Smart card

**Difference from badge:**


**smarter/more secure**

- chip-based

**Memory:**

- Card with brain/chip.

**Difference:**


**Key fob**


**Usually:**

- small token/keychain

**Smart card**


**Usually:**

- card format with chip
- CompTIA may test this distinction.
- Mobile Digital Key
- Smartphone used as credential.

**Examples:**


**NFC phone unlock**


**Bluetooth access app**

- mobile badge

**Purpose:**

- phone replaces card/key.

**Scenario**

- Employee unlocks office using smartphone app.

> **Answer:** 
- ✅ Mobile digital key

**Common in:**


**hotels**

- offices
- Memory:

**Phone = key**


**Keys**

- Traditional physical key.
- Simple mechanical access.

**Purpose:**

- unlock doors/cabinets.

**Scenario**

- Server cabinet secured with traditional metal key.

> **Answer:** 
- ✅ Keys
- Low tech, still common.

**Memory:**

- The old-school original access token.
- Biometrics

> 💡 **Key Tip:** Authentication using body traits


**Retina Scanner**

- Scans retina/eye pattern.
- Very secure.
- Usually high-security areas.

**Scenario**

- Secure lab scans employee eye pattern before entry.

> **Answer:** 
- ✅ Retina scanner

**Memory:**

- Eye scan.

**Fingerprint Scanner**

- Scans fingerprint.

**Common on:**


**laptops**


**phones**

- doors

**Scenario**

- User unlocks laptop with finger.

> **Answer:** 
- ✅ Fingerprint scanner
- Very common.

**Memory:**

- Finger = fingerprint.

**Palm Print Scanner**

- Scans palm characteristics.
- Less common.
- Higher accuracy.

**Scenario**

- Employee places palm on scanner to access restricted room.

> **Answer:** 
- ✅ Palm print scanner

**Memory:**

- Hand scanner.

**Facial Recognition Technology (FRT)**

- Uses face geometry.

**Examples:**


**phone unlock**

- building access

**Scenario**

- Device unlocks by scanning user face.

> **Answer:** 
- ✅ Facial recognition technology

**Memory:**

- Face unlock.

**Voice Recognition Technology**

- Uses voice pattern.

**Examples:**

  - voice authentication

**Scenario**

- System verifies speaker voice before granting access.

> **Answer:** 
- ✅ Voice recognition

**Memory:**

- Voiceprint.

**Lighting**

- Security through visibility.

**Purpose:**


**deter crime**


**improve camera footage**

- increase visibility
- Used:

**parking lots**


**building perimeter**

- entrances

**Scenario**


**Company installs bright lights around building exterior to discourage**

- trespassing.

> **Answer:** 
- ✅ Lighting

**Why useful:**

- Criminals prefer darkness.

**Memory:**

- Light = visibility security.

**Magnetometers**

- Detect metal objects.

**Examples:**

- weapon detection

**Common:**


**airports**


**courthouses**

- events

**Looks like:**

- walk-through metal detector.

**Scenario**

- Visitors walk through device that detects concealed metal weapons.

> **Answer:** 
- ✅ Magnetometer

**Purpose:**

- physical screening.

**Memory:**

- Metal detector gate.
- Logical security

> 💡 **Key Tip:** Protecting systems/data using software rules, permissions, and authentication


**Principle of Least Privilege**

- Very important.

**Meaning:**

- Users only get minimum permissions needed to do their job.
- Not more.
- Why?

**reduce risk**


**limit damage**

- improve security

**Example**

- Intern only needs read access.

**Do NOT give:**


**admin rights**

- delete rights

**Scenario**

- A new employee only needs to view files, not edit or delete them.

> **Answer:** 
- ✅ Principle of least privilege

**Memory:**

- Give only what is necessary.

**Zero Trust Model**


**Security mindset:**

- Trust nobody by default.
- Even internal users/devices must verify.

**Old mindset:**

- inside network = trusted

**Zero Trust:**

- always verify

**Principles:**

- verify identity

**verify device**


**least privilege**

- continuous validation

**Scenario**


**Company requires authentication for every access request, even from**

- internal network.

> **Answer:** 
- ✅ Zero Trust

**Memory:**

- Trust nothing, verify everything.

**Access Control Lists (ACLs)**

- Rules defining who can access what.

**Can specify:**


**allow**


**deny**

- permissions

**Used on:**


**files**


**folders**

- network devices

**Example:**


**User A: read**

- User B: deny
- Scenario

**Administrator configures file permissions specifying which users may**

- read or write.

> **Answer:** 
- ✅ ACL

**Memory:**

- Permission rule list.

**Multifactor Authentication (MFA)**

- Requires 2+ authentication factors.

**Email**

- Code sent to email.

> **Scenario:** 
- Login sends verification code to email.

> **Answer:** 
- ✅ Email MFA

**Hardware Token**

- Physical device generates code.

**Examples:**

  - RSA token
  - USB token

> **Scenario:** 
- User enters code from physical token device.

> **Answer:** 
- ✅ Hardware token

**Authenticator Application**

- Mobile app generates codes.

**Examples:**


**Google Authenticator**

- Microsoft Authenticator

> **Scenario:** 
- User approves login from authenticator app.

> **Answer:** 
- ✅ Authenticator app

**SMS**

- Text message code.

> **Scenario:** 
- Verification code texted to phone.

> **Answer:** 
- ✅ SMS

**Voice Call**

- Code delivered by phone call.

> **Scenario:** 
- User receives automated call with verification code.

> **Answer:** 
- ✅ Voice call

**TOTP (Time-Based One-Time Password)**

- Code changes every short period (like 30 sec).
- Often from authenticator app.

**Scenario**

- Login requires 6-digit code that refreshes every 30 seconds.

> **Answer:** 
- ✅ TOTP

**Memory:**

- Time-based changing code.

**OTP (One-Time Password/Passcode)**

- Single-use code.

**Can be:**


**email**


**SMS**

- app
- Not necessarily time-based.

**Scenario**

- User receives single-use verification code.

> **Answer:** 
- ✅ OTP

**Difference:**


**OTP = one-time code**

- TOTP = time-based one-time code

**Security Assertions Markup Language (SAML)**

- A mouthful, yes.
- Used to exchange authentication data between systems.
- Often supports SSO.

**Example:**

- Login once through company identity provider.

**Scenario**


**User authenticates with company account to access third-party cloud**

- app.

> **Answer:** 
- ✅ SAML

**For A+, think:**

- SAML = authentication sharing/federation.
- Don’t overcomplicate.

**Single Sign-On (SSO)**

- One login grants access to multiple systems.

**Benefits:**


**convenience**

- fewer passwords

**Scenario**

- Employee signs in once and automatically accesses email, HR portal, and Teams.

> **Answer:** 
- ✅ SSO
- Memory:
- One login, many apps.
- Just-in-Time Access

> 💡 **Key Tip:** PAM ensures that privileged accounts are used securely by limiting access to only what is necessary for a given task. It includes Just-in-Time permissions, password vaulting, and temporal accounts to prevent unauthorized use.


**PAM (Privileged Access Management)**

- Controls/administers privileged accounts.

**Focus:**


**admin credentials**


**elevated permissions**

- auditing

**Scenario**


**Company tightly controls administrator credentials and privileged**

- sessions.

> **Answer:** 
- ✅ PAM

> **Think:** 
- Manage powerful accounts.

**Mobile Device Management (MDM)**

- Manage company mobile devices remotely.

**Functions:**


**remote wipe**


**enforce policies**

- app control encryption

**Scenario**

- Admin remotely wipes lost company phone.

> **Answer:** 
- ✅ MDM

**Memory:**

- Mobile security management.

**Data Loss Prevention (DLP)**

- Prevent sensitive data leakage.

**Monitors/blocks:**


**file transfers**


**email attachments**

- uploads

**Scenario**


**Company blocks employees from emailing customer database**

- externally.

> **Answer:** 
- ✅ DLP

**Memory:**

- Stop data from leaving.

**Identity Access Management (IAM)**


**Broad management of:**


**users**


**roles**

- permissions authentication
- Big umbrella concept.

**Includes:**


**provisioning users**

- managing access

**Scenario**

- Company centrally manages employee identities and permissions.

> **Answer:** 
- ✅ IAM

**Memory:**

- Who gets access to what.

**Directory Services**

- Centralized user/resource database.

**Example:**

- Microsoft Active Directory

**Stores:**


**users**


**groups**

- policies

**Scenario**


**Administrator manages users and computers from centralized domain**

- service.

> **Answer:** 
- ✅ Directory services

### 2.2 Microsoft Windows OS security settings

- Defender Antivirus

> 💡 **Key Tip:** Microsoft Defender Antivirus is Windows’ built-in antivirus/anti- malware tool. It helps detect: viruses ransomware spyware trojans suspicious files Think of it as Windows' security guard.

- Activate / Deactivate Defender Antivirus

**How to enable/disable**


**Path:**

- Settings > Privacy & Security > Windows Security > Virus & threat protection

**Then:**

  - Manage settings
  - Turn Real-time protection ON/OFF

**Important exam note**


**CompTIA may ask:**


**Why disable antivirus?**


**Valid reasons:**

  - Installing another antivirus
  - Software conflict testing
- Troubleshooting false positives

**Scenario**


**User says:**

- “My PC is slow, so I turned off antivirus permanently.”

**Problem**

- Now system is exposed to malware.

**Troubleshooting**


#### 1. Open Windows Security


#### 2. Check if Real-time protection is OFF


#### 3. Re-enable protection


#### 4. Run quick/full scan


#### 5. Educate user

- Best practice: disable temporarily only.

**Update Definitions**


**Definition = malware signature database**


**Antivirus without updates is like a security guard using last year’s**

- criminal photos.

**Update path**

- Windows Security > Virus & threat protection > Protection updates

**Then:**

- Check for updates

**Or update Windows:**

- Settings > Windows Update
- Scenario

**User says:**

- “Defender says definitions are outdated.”

**Troubleshooting**


#### 1. Check internet connection


#### 2. Open Protection updates


#### 3. Click Check for updates


#### 4. Run Windows Update


#### 5. Restart if needed


**Possible causes:**


**no internet**


**paused updates**

- Windows Update service issue
- Firewall

> 💡 **Key Tip:** Rules: allow traffic block traffic Think: Antivirus = protects files Firewall = protects network connections


**Activate / Deactivate Firewall**


**Path:**

- Control Panel > System and Security > Windows Defender Firewall

**or**

- Settings > Windows Security > Firewall & network protection

**Profiles:**

  - Domain
  - Private
  - Public

**Exam tip**

- Public network = stricter security.

**Example:**


**Coffee shop Wi-Fi → Public profile**

- Home Wi-Fi → Private profile

**Scenario**


**User says:**

- “Can’t access company app after changing firewall settings.”

**Troubleshooting**


#### 1. Check firewall status


#### 2. See if firewall is OFF


#### 3. Re-enable firewall


#### 4. Test app again


#### 5. Review blocked app rules

- Sometimes users disable firewall to “fix internet” (classic bad move).

**Port Security**

- A port is a communication doorway.

**Examples:**


**HTTP = 80**


**HTTPS = 443**

- RDP = 3389
- FTP = 21
- Firewall can block/open ports.

**Why secure ports?**

- Open unnecessary ports = security risk.

**Example:**

- Port 3389 (RDP) open to internet = attack target.

**Configure ports**


**Path:**

- Windows Defender Firewall > Advanced settings

**Then:**


**Inbound Rules**

- Outbound Rules

**You can:**

- Allow port
- Block port

**Scenario**


**User says:**

- “Remote Desktop stopped working.”

**Troubleshooting**


#### 1. Check if RDP enabled


#### 2. Check firewall inbound rule


#### 3. Verify port 3389 allowed


#### 4. Confirm network connectivity


**Possible issue:**

- Firewall blocks 3389.

**Application Security**

- Firewall can allow/block apps.
- Instead of opening all ports, allow only trusted applications.

**Example:**


**allow browser**


**allow VPN**

- allow remote support tool

**Block:**


**unknown app**

- suspicious executable

**Configure allowed apps**


**Path:**

- Windows Defender Firewall > Allow an app through firewall

**You can:**


**check/uncheck apps**

- choose Private/Public access

**Scenario**


**User says:**


**“Zoom works at home but not on office Wi-Fi.”**

- (Example app: Zoom)

**Troubleshooting**


#### 1. Check firewall rules


#### 2. Verify Zoom allowed


#### 3. Confirm network profile


#### 4. Test on private/public network


**Possible cause:**

- App blocked by firewall.

**User and Groups**


**Local vs Microsoft Account**


**Local Account**

- Account exists only on that PC.

**Features:**

  - offline login no Microsoft cloud sync traditional Windows account

**Example:**

- School lab computer.

**Microsoft Account**


**Connected to Microsoft services like:**

  - OneDrive
  - Microsoft Store settings sync

**Example:**

- Personal laptop using Outlook account.

**Exam Memory Trick**

  - Local = Local computer only
  - Microsoft = Microsoft cloud/services

**Scenario**


**User says:**

- “My wallpaper and settings don’t sync to my new PC.”

**Troubleshooting**


#### 1. Check if using local account


#### 2. Sign in with Microsoft account


#### 3. Enable sync settings


**Standard Account**

- Regular user account.

**Can:**


**use apps**


**browse internet**

- change own settings

**Cannot:**


**install system-wide software**


**change security settings**

- manage other users

**Best for:**

- everyday users

**Exam Memory Trick**


**Standard = Safe**


**Least privilege principle:**

- Give only permissions needed.

**Scenario**


**User says:**

- “I can’t install software.”
- Troubleshooting

#### 1. Check account type


#### 2. Verify if user is Standard


#### 3. Use admin credentials if approved


**Administrator**

- Full control of system.

**Can:**


**install software**


**change system settings**


**manage users**

- disable security tools

**Danger:**

- Malware running as admin can damage whole system.

**Exam Memory Trick**

- Admin = All permissions

**Scenario**


**User says:**

- “I need to create accounts for new employees.”

**Solution**

- Must use Administrator account.

**Guest User**

- Temporary limited access account.

**Can:**

- basic computer use
- Cannot:

**install software**

- modify system settings

**Usually:**

- disabled by default in modern Windows

**Exam Memory Trick**

- Guest = Temporary visitor

**Scenario**

- Visitor needs internet access on office PC.

**Best choice:**


**Guest account**

- not Administrator

**Power User**


**Old Windows group with more permissions than Standard but less than**

- Administrator.
- Mostly legacy/older Windows concept.
- CompTIA may mention it historically.

**Exam Memory Trick**


**Permission level order:**

- Guest < Standard < Power User < Administrator

**Mini Exam Tips**


**Best security practice?**

- Use Standard account daily.

**When use Administrator?**


**Only for:**

  - maintenance installations system changes

**Biggest exam concept:**


**Least privilege**

- = users should only have permissions necessary for their job
- Log-in OS Options

> 💡 **Key Tip:** These are different ways users authenticate (prove identity) in Windows


#### 1. Username and Password

- Most traditional login method.

**User enters:**


**username**

- password

**Exam Memory Trick**


**Something you KNOW**

- = password

**Scenario**


**User says:**

- “I forgot my password.”

**Troubleshooting**


#### 1. Verify username


#### 2. Reset password


#### 3. Confirm keyboard layout/Caps Lock


#### 2. PIN (Personal Identification Number)

- Short number used to log into device.

**Important:**


**PIN is tied to THAT device only**

- safer than many people think

**Exam Memory Trick**


**PIN = Local device login**

- Microsoft password works across devices.
- PIN usually works only on one PC.

**Scenario**

- User changes Microsoft password but still logs in using old PIN.

**Why?**

- PIN is device-specific.

#### 3. Fingerprint

- Biometric authentication.

**Uses:**


**fingerprint scanner**

- Windows Hello

**Exam Memory Trick**


**Something you ARE**

- = biometrics

**Scenario**


**User says:**

- “Fingerprint login stopped working.”

**Troubleshooting**


#### 1. Clean scanner


#### 2. Re-add fingerprint


#### 3. Update driver


#### 4. Check biometric service


#### 4. Facial Recognition

- Camera scans user’s face.

**Also part of:**


**Windows Hello**

- Requires compatible camera.

**Scenario**

- Laptop cannot use face unlock.

**Troubleshooting**


#### 1. Verify IR-compatible camera


#### 2. Check Windows Hello setup


#### 3. Update camera drivers


#### 5. SSO (Single Sign-On)

- User logs in once and accesses multiple systems.

**Example:**


**One company login for:**


**email**


**Teams**

- company portal

**Exam Memory Trick**

- One login → many services

**Scenario**

- User signs into Windows and automatically accesses company apps.
- That is SSO.

#### 6. Passwordless / Windows Hello

- Windows Hello allows login without traditional password.

**Methods:**


**PIN**


**fingerprint**

- facial recognition

**Benefits:**


**faster**

- more secure against phishing

**Exam Memory Trick**

- Windows Hello = modern passwordless authentication.

**Common CompTIA Concepts**


**Authentication Factors**


**Factor               Example**


**Something you know Password, PIN**


**Something you have   Security key**

- Something you are    Fingerprint, face

**NTFS vs Share Permissions**


**Permissions can be set on a folder using both NTFS and sharing option**


**File and Folder Attributes**

- Special file settings.

**Common attributes:**

  - Read-only
  - Hidden
  - Archive
  - System

**Inheritance**

- Permissions automatically pass from parent folder to child folder.

**Example:**

- Company Folder
- → all subfolders inherit same permissions.
- Run as Administrator vs Standard User

**Standard User**

- Limited permissions.

**Run as Administrator**

- Temporarily gives admin privileges.

**Scenario**

- App cannot install.

**Troubleshooting**


#### 1. Right-click app


#### 2. Select “Run as administrator”


#### 3. Approve UAC prompt


**User Account Control (UAC)**

- Security feature that asks permission before admin-level changes.

**Example popup:**

- “Do you want to allow this app to make changes?”

**Scenario**

- Unknown app suddenly triggers UAC popup.

**Best action**


**deny access**

- verify app legitimacy

**BitLocker**

- BitLocker encrypts entire drive.

**Protects data if device is:**


**stolen**

- lost

**Usually uses:**


**TPM chip**

- recovery key

**Exam Memory Trick**

- BitLocker = Full disk encryption

**Scenario**

- Employee laptop stolen.

**Why is data protected?**

- BitLocker encryption.

**BitLocker To Go**


**Encrypts:**


**USB drives**

- external drives
- Portable version of BitLocker.

**Exam Memory Trick**

- To Go = removable drives

**Scenario**

- Company USB contains sensitive files.

**Best solution**

- Enable BitLocker To Go.

**Encrypting File System (EFS)**


**Encrypts:**

- individual files/folders
- NOT full drive.
- Works only on NTFS.

**Exam Memory Trick**


**BitLocker = whole drive**

- EFS = individual files

**Scenario**

- User wants only HR folder encrypted.

**Best solution**

- Use EFS.
- Active Directory (AD)

> 💡 **Key Tip:** Active Directory is Microsoft’s centralized system for managing: users computers permissions policies Mostly used in company/business networks.


**Joining Domain**

- Adds computer to company network domain.

**Benefits:**

  - centralized login
  - Group Policy company resource access

**Exam Memory Trick**


**Workgroup = standalone**

- Domain = centrally managed

**Scenario**

- New office PC cannot use company login.

**Troubleshooting**


#### 1. Check network connection


#### 2. Verify domain name


#### 3. Join domain


#### 4. Restart PC


**Assigning Log-in Script**

- Script runs automatically after user logs in.

**Common uses:**


**map network drives**


**printers**

- set environment settings

**Usually:**


**PowerShell**

- batch scripts

**Scenario**

- Employees should automatically connect to shared drive after login.

**Solution**

- Assign login script in AD.

**Moving Objects Within Organizational Units (OU)**

- OU = folder/container in AD.

**Objects:**


**users**


**computers**

- groups
- Moving objects changes:
  - policies permissions

**Exam Memory Trick**

- OU helps organize management

**Scenario**

- HR employee not receiving HR policies.

**Troubleshooting**


#### 1. Check user location in AD


#### 2. Move user into correct OU


#### 3. Force policy update


**Assigning Home Folders**

- Personal network storage folder for users.

**Example:**

- H:\

**Benefits:**

  - centralized storage backups access from multiple PCs

**Scenario**

- User cannot access personal company files on another PC.

**Troubleshooting**


#### 1. Verify home folder path


#### 2. Check permissions


#### 3. Confirm network access


**Applying Group Policy**

- Group Policy centrally controls Windows settings.

**Examples:**


**password rules**


**desktop wallpaper**


**disable Control Panel**

- security settings

**Exam Memory Trick**

- Group Policy = automatic company rules

**Scenario**

- Company wants all PCs to lock after 5 minutes idle.

**Solution**

- Apply Group Policy.

**Selecting Security Groups**

- Groups simplify permission management.

**Instead of assigning permissions one-by-one:**


**add users to group**

- assign permissions to group

**Examples:**


**HR Group**


**IT Admins**

- Sales Team

**Exam Memory Trick**

- Permissions are usually assigned to groups, not individual users.

**Scenario**

- New HR employee needs HR folder access.

**Solution**

- Add user to HR security group.

**Configuring Folder Redirection**

- Redirects folders to network location.

**Common redirected folders:**


**Desktop**


**Documents**

- Downloads

**Benefits:**


**backup**


**roaming access**

- centralized storage

**Scenario**

- Employee changes PC but files still appear automatically.

**Why?**

- Folder redirection.

### 2.3 Wireless security protocols and authentication

methods

> 💡 **Key Tip:** These protect Wi-Fi networks from unauthorized access and attacks. Main idea: authentication = who can join encryption = protects transmitted data


**Protocols and encryption**


**Protocol/Encryption Status**


**WEP                   Obsolete**


**TKIP                  Weak/legacy**


**WPA2                  Secure**


**WPA3                  Most secure**

- AES                   Strong encryption

#### 1. WPA2


**Full name:**


**Wi-Fi Protected Access 2**

- Most common older modern Wi-Fi security standard.

**Uses:**


**strong encryption**

- home/business Wi-Fi

**Usually paired with:**

- AES encryption

**Exam Memory Trick**

- WPA2 + AES = good standard answer

**Scenario**

- User’s router still uses WEP and network is insecure.

**Best solution**

- Upgrade to WPA2 or WPA3.

#### 2. WPA3

- Newest and more secure Wi-Fi protection standard.

**Better against:**


**password guessing**

- brute-force attacks
- More secure than WPA2.

**Exam Memory Trick**


**Security order:**


**WEP < WPA < WPA2 < WPA3**

- (Newer = stronger)

**Scenario**


**Company upgrades wireless security for better protection against password**

- attacks.

**Best solution**

- Use WPA3.

#### 3. TKIP

- Full name:

**Temporal Key Integrity Protocol**

- Older encryption used with WPA.
- Weak and outdated now.

**Exam Memory Trick**


**TKIP = old**

- Avoid if possible.

**Scenario**

- Old device only supports WPA/TKIP.

**Issue**

- Weak security and slower performance.

#### 4. AES


**Full name:**


**Advanced Encryption Standard**

- Modern strong encryption.

**Used with:**


**WPA2**

- WPA3
- Fast and secure.

**Exam Memory Trick**


**AES = secure modern encryption**


**CompTIA often wants:**

- WPA2 + AES
- WPA3 + AES

**Authentication**


**RADIUS (Remote Authentication Dial-In User Service)**

  - centralized authentication for network access

**Common use:**

  - enterprise Wi-Fi
  - VPN network access control

**Instead of every Wi-Fi device storing usernames/passwords:**


**Access point asks RADIUS server:**

  - “Can Lucas connect?”
- RADIUS checks and responds.

**Scenario**

- Company Wi-Fi requires employees to log in with company credentials.
- Authentication handled by central server.

> **Answer:** 
- ✅ RADIUS

**Common with:**

  - 802.1X
  - WPA2/WPA3 Enterprise

**Memory:**


**RADIUS = centralized Wi-Fi login checker**


**TACACS+ (Terminal Access Controller Access-Control System Plus)**


**Similar idea to RADIUS, but more often used for:**

  - device administration
- network equipment management

**Examples:**


**router admin login**

- switch admin login
- Not usually end-user Wi-Fi.

**Scenario**


**Network admins authenticate when managing routers/switches through**

- centralized server.

> **Answer:** 
- ✅ TACACS+
- Difference:

**RADIUS**

- user/network access

**TACACS+**

- admin/device management

**Memory:**


**TACACS+ = admin control**


**Kerberos**

- Authentication protocol using tickets.
- Common in Windows domain environments.

**Example:**

- User logs in once and gets ticket to access services.
- Avoids repeatedly sending password.

**Often used with:**

- Active Directory

**Scenario**


**User authenticates once to domain and accesses multiple internal**

- resources using tickets.

> **Answer:** 
- ✅ Kerberos

**Benefits:**


**mutual authentication**

- ticket-based

**Memory:**


**Kerberos = ticket authentication**


**(Three-headed dog guarding access in mythology.)**


**Diameter**

- Modern successor to RADIUS.

**Used in:**


**telecom**


**mobile networks**

- AAA services

**AAA =**


**Authentication**


**Authorization**

- Accounting
- Less common in A+ scenarios, but know concept.

**Scenario**


**A provider uses newer protocol replacing RADIUS for**

- authentication/accounting.

> **Answer:** 
- ✅ Diameter

> **Think:** 
- Newer RADIUS cousin.

**Memory:**


**Diameter = upgraded RADIUS**


**LDAP (Lightweight Directory Access Protocol)**

- Used to access directory services.

**Examples:**


**user database**

- directory lookup

**Often with:**

- Active Directory

**Stores:**


**users**


**groups**

- organizational info

**Scenario**

- Application queries centralized directory for user account information.

> **Answer:** 
- ✅ LDAP

> **Think:** 
- Directory lookup.
- Not directly authentication itself (though used with auth systems).

**Memory:**


**LDAP = directory phonebook**


**802.1X**

- Port-based network access control.
- Controls whether device/user can connect to network.

**Often used for:**


**enterprise Wi-Fi**

- wired authentication too

**Works with:**

- RADIUS

**Flow:**


#### 1. connect


#### 2. authenticate


#### 3. access granted


**Scenario**


**Company requires devices to authenticate before network access is**

- granted.

> **Answer:** 
- ✅ 802.1X

**Common combo:**

- 802.1X + RADIUS

**Memory:**


**Gatekeeper before network entry**


**EAP (Extensible Authentication Protocol)**

- Framework for authentication methods.
- Not a single method.
- Used inside 802.1X.

**Supports:**


**certificates**


**passwords**

- tokens

**Examples:**


**EAP-TLS**

- PEAP

**For A+:**

- Just know EAP = authentication framework.

**Scenario**

- Wireless authentication framework supports multiple credential types.

> **Answer:** 
- ✅ EAP

**Memory:**


**Authentication container/framework**


**Multifactor Authentication (MFA)**

- Uses multiple authentication factors.

**Examples:**


**password + phone code**

- PIN + fingerprint

**Exam Memory Trick**

- At least two different factor types.

**Not:**

  - password + another password            ❌

### 2.4 Malware and tools/methods for detection,

removal, and prevention
- Malware

> 💡 **Key Tip:** Malware = malicious software designed to: damage systems steal data spy on users make money illegally Malware           Main Function Trojan            Fake legitimate app Rootkit           Hides deeply Virus             Infects files Spyware           Spies on user Ransomware        Encrypts files Keylogger         Records typing Boot sector virus Infects startup Cryptominer       Uses CPU/GPU Stalkerware       Secret monitoring Fileless          Runs in memory


#### 1. Trojan


**Function**

- Pretends to be legitimate software to trick users into installing malware.
- Usually used to:

**steal data**


**open backdoors**

- install more malware

**Explanation**

- Unlike a virus, a Trojan does NOT spread itself automatically.
- User normally installs it manually.

**Scenario**

- User downloads a “free premium game” from random website.

**After installation:**


**computer becomes slow**

- strange popups appear

**Likely malware:**

- Trojan.

#### 2. Rootkit


**Function**

- Hides malware and attacker activity deep inside the operating system.
- Can give attackers administrator/root access.

**Explanation**

- Very difficult to detect because it hides processes and files.

**Scenario**


**Antivirus shows nothing, but:**

- system acts strangely unknown admin accounts appear

**Possible:**

- Rootkit infection.

#### 3. Virus


#### 3. Virus


**Function**

- Infects files/programs and spreads when infected files are opened.

**Explanation**

- Needs user action to spread.

**Often spreads through:**


**USB drives**

- email attachments

**Scenario**

- Employee opens infected attachment and many files become infected.

**Likely:**

- Virus.

#### 4. Spyware


**Function**

- Secretly monitors user activity and collects information.

**Explanation**

- Can track:

**browsing habits**


**passwords**

- personal information

**Scenario**


**User installs free software and suddenly receives targeted ads**

- everywhere.

**Possible:**

- Spyware.

#### 5. Ransomware


**Function**

- Encrypts files and demands payment to unlock them.

**Explanation**

- One of the biggest business threats today.

**Scenario**


**All documents suddenly become inaccessible and message says:**


**“Pay Bitcoin to recover files.”**


**Likely:**

- Ransomware.

#### 6. Keylogger


**Function**

- Records keyboard input.
- Explanation

**Attackers use it to steal:**


**passwords**

- banking credentials

**Scenario**

- User’s accounts get hacked even though passwords were never shared.

**Possible:**

- Keylogger infection.

#### 7. Boot Sector Virus


**Function**

- Infects boot sector/MBR so malware loads before Windows starts.

**Explanation**

- Can interfere with startup process.

**Scenario**

- PC fails to boot properly after malware infection.

**Possible:**

- Boot sector virus.

#### 8. Cryptominer


**Function**

- Uses victim’s CPU/GPU to mine cryptocurrency.

**Explanation**

- Consumes system resources heavily.

**Symptoms:**


**overheating**


**loud fans**

- high CPU usage

**Scenario**

- Computer becomes extremely slow even when no apps are open.
- Task Manager shows unusually high CPU usage.

**Possible:**

- Cryptominer.

#### 9. Stalkerware


**Function**

- Secretly monitors a victim’s activity.

**Explanation**

- Often installed without consent on phones/devices.

**Tracks:**


**messages**


**calls**

- location

**Scenario**

- Person suspects partner is secretly monitoring phone activity.

**Possible:**

- Stalkerware.

#### 10. Fileless Malware


**Function**

- Runs mainly in memory using legitimate Windows tools.

**Explanation**


**Often uses:**

  - PowerShell scripts system processes
- Hard for antivirus to detect.

**Scenario**

- System behaves suspiciously but no malicious files are found.

**Possible:**

- Fileless malware.

**Adware**

- Displays unwanted advertisements on a device.

**Potentially Unwanted Program (PUP)**


**Function**

- Software user technically agreed to install, but it behaves undesirably.

**Explanation**

- Usually bundled with free software.

**Examples:**


**toolbars**

- fake cleaners unnecessary optimizers

**May:**


**slow PC**


**change browser settings**

- collect usage data

**Scenario**

- User installs free PDF converter.

**After installation:**


**browser toolbar appears**


**search engine changed**

- PC slower

**Likely:**

- PUP.

**Troubleshooting**


#### 1. Uninstall unwanted software


#### 2. Remove startup entries


#### 3. Scan system


#### 4. Educate user about bundled installers


**Tools and methods**

- Recovery Console

**Function**


**Troubleshooting environment used when Windows cannot boot**

- properly.
- Used to:

**repair startup**


**restore system**

- run repair commands

**Scenario**

- PC stuck in boot loop after malware infection.

**Solution**

- Use recovery console/startup repair.

**Exam Memory Trick**


**Recovery console = repair broken Windows**


**EDR (Endpoint Detection and Response)**

- Monitors devices for suspicious activity and responds to threats.
- Endpoint = laptop, desktop, server.

**Detects:**


**unusual behavior**


**attacks**

- malware activity

**Scenario**


**Company security team gets alert that employee PC is communicating**

- with malicious server.
- EDR detects it.

**Exam Memory Trick**

- EDR = detect and respond on devices
- MDR (Managed Detection and Response)

**Function**


**Third-party security service that monitors and responds to threats for a**

- company.
- Humans + security tools.

**Scenario**

- Small company lacks cybersecurity team.
- They hire MDR provider to monitor threats 24/7.

**Exam Memory Trick**


**MDR = outsourced security monitoring**

- XDR (Extended Detection and Response)

**Function**


**Combines security data from multiple systems:**


**endpoints**


**email**


**servers**

- network
- Provides broader threat visibility.

**Scenario**

- Attack starts from phishing email then spreads to endpoints.
- XDR connects all related alerts together.
- Exam Memory Trick

**XDR = wider visibility across systems**

- Antivirus

**Function**

- Detects and removes viruses and known malware.

**Uses:**


**signatures**

- behavior detection

**Scenario**

- USB infects PC with malware.
- Antivirus detects and quarantines infected file.

**Exam Memory Trick**


**Antivirus mainly targets known threats**

- Anti-malware

**Function**


**Broader protection against many malware types:**


**spyware**


**ransomware**


**trojans**

- worms

**Scenario**

- Security software removes spyware and ransomware together.
- That is anti-malware protection.

**Exam Memory Trick**

- All antivirus is anti-malware, but anti-malware covers more threats.
- Email Security Gateway

**Function**

- Filters dangerous emails before they reach users.

**Blocks:**


**phishing**


**spam**

- malicious attachments

**Scenario**


**Company blocks fake banking email automatically before employees**

- receive it.

**Likely:**

- Email security gateway.

**Exam Memory Trick**


**Gateway filters dangerous email traffic**

- Software Firewalls

**Function**

- Controls network traffic on device.

**Can:**


**allow connections**

- block suspicious traffic

**Scenario**

- Application cannot access internet because firewall blocks it.

**Exam Memory Trick**


**Firewall controls network communication**

- User Education (Anti-Phishing Training)

**Function**

- Teaches users how to avoid attacks.

**Common training:**


**suspicious emails**


**fake links**

- social engineering
- Humans are often weakest security point.

**Scenario**

- Employee receives fake “reset your password” email.
- Training helps them recognize phishing attempt.

**Exam Memory Trick**


**Best defense sometimes = educated users**

- OS Reinstallation

**Function**

- Completely reinstall operating system.

**Used when:**

- severe malware infection
  - corrupted system troubleshooting failure

**Scenario**

- Ransomware heavily damaged system files.

**Best solution:**

- Backup data and reinstall OS.

### 2.5 Social engineering attacks, threats, and

vulnerabilities+
- Social Engineering

> 💡 **Key Tip:** Psychological manipulation to trick users into revealing information, granting access, or performing actions.


**Phishing**

  - 1. Vishing
  - Attack via phone call.
  - “V” = voice.
  - Attacker pretends:
  - bank tech support government manager
  - Goal:
  - get passwords
  - OTP codes payment

**Scenario**


**Caller claims:**

- I’m from IT support. Tell me your password.

> **Answer:** 
- ✅ Vishing

#### 2. Smishing


**SMS phishing**

- Attack through text message.
- “S” = SMS.

**Examples:**


**fake parcel delivery**


**fake bank alert**

- fake OTP issue

**Scenario**


**Text message:**

- Your package is delayed. Click here.

> **Answer:** 
- ✅ Smishing

**Memory:**

- S = SMS

#### 3. QR Code Phishing (Quishing)

- Attacker hides malicious link in QR code.
- User scans and opens fake site.

**Common:**

- fake payment QR

**fake login QR**

- restaurant posters

**Scenario**


**Employee scans QR code from poster and enters credentials on fake**

- login page.

> **Answer:** 
- ✅ QR code phishing

**Memory:**

- QR = hidden phishing link

#### 4. Spear Phishing

- Targeted phishing.
- Not mass email.
- Attacker researches victim first.
- Personalized.

**Example:**


**knows your name**


**company**

- manager
- Higher success rate.

**Scenario**


**Email says:**

- Hi Lucas, please review attached Q2 sales report.
- Looks personalized.

> **Answer:** 
- ✅ Spear phishing

**Difference:**

  - Phishing = broad attack
  - Spear phishing = targeted

**5. Whaling**

  - Spear phishing attacks use detailed information about the target to create convincing messages that appear legitimate. This makes victims more likely to fall for the scam compared to generic phishing attempts.

**Targets high-level executives:**

  - CEO
  - CFO director
- “Big fish.”

**Scenario**

- Attacker sends fake legal notice to CEO requesting credentials.

> **Answer:** 
- ✅ Whaling

**Memory:**

- Whale = big target

**Shoulder Surfing**

- Watching someone enter sensitive info.

**Can be:**


**password**


**PIN**

- card number
- Usually physical observation.

**Scenario**

- Attacker watches employee type password in coffee shop.

> **Answer:** 
- ✅ Shoulder surfing

**Protection:**


**privacy screen**

- awareness

**Memory:**

- Literally looking over shoulder.

**Tailgating**

- Unauthorized person follows authorized user into secure area.
- No authentication.
- Physical breach.

**Scenario**

- Attacker follows employee through badge-protected door.

> **Answer:** 
- ✅ Tailgating

**Memory:**


**Car analogy:**


**following too closely**


**Impersonation**

- Pretending to be someone trusted.

**Examples:**

- fake technician

**fake manager**

- fake vendor

**Goal:**

- gain trust.

**Scenario**

- Attacker wears IT badge and requests server room access.

> **Answer:** 
- ✅ Impersonation

**Memory:**


**“Pretend to be someone else.”**


**Dumpster Diving**

- Searching trash for sensitive information.

**Looking for:**


**printed passwords**


**invoices**


**customer records**

- hardware labels
- Very old-school but still testable.

**Scenario**

- Attacker searches company trash and finds printed employee directory.

> **Answer:** 
- ✅ Dumpster diving

**Protection:**

- shredding documents

**Memory:**

- Trash treasure hunting

**Threats**


**Denial of Service (DoS)**

- Attack makes service/system unavailable.

**Goal:**

  - overload target crash service deny legitimate users
- Usually from one source/device.

**Scenario**

- A single attacker floods company website with requests until it crashes.

> **Answer:** 
- ✅ DoS

> **Think:** 

**One attacker → one flood source**


**Memory:**


**Denial of service =**

- deny access

**Distributed Denial of Service (DDoS)**

- Same idea, but attack comes from many devices.
- Often botnet.
- Harder to block.
- “Distributed” = multiple systems.

**Scenario**

- Thousands of infected computers flood website traffic.

> **Answer:** 
- ✅ DDoS

**Difference:**


**DoS = one source**

- DDoS = many sources

**Memory:**


**D = distributed/many**


**Evil Twin**

- Fake Wi-Fi hotspot pretending to be legitimate network.
- Attacker wants users to connect.

**Then can:**


**capture traffic**

- steal credentials

**Example:**


**Real Wi-Fi:**

- CoffeeShop_Wifi

**Fake:**

- CoffeeShop_FreeWifi

**Scenario**

- Attacker creates wireless network with same name as hotel Wi-Fi.

> **Answer:** 
- ✅ Evil twin

> **Think:** 
- Fake Wi-Fi twin.

**Protection:**


**verify SSID**


**avoid unknown Wi-Fi**

- VPN

**Zero-Day Attack**

- Attack exploits vulnerability before patch exists.

**Meaning:**


**software flaw discovered**

- no fix yet
- Very dangerous.

**“Zero-day” =**

- vendor had zero days to patch.

**Scenario**

- New browser vulnerability exploited before vendor releases update.

> **Answer:** 
- ✅ Zero-day attack

**Memory:**

- Zero days to prepare.

**Spoofing**

- Pretending to be another system/user/device.

**Can fake:**


**IP**

- email

**MAC**


**caller ID**

- website

**Goal:**

- gain trust or bypass filters.

**Scenario**

- Attacker sends email appearing to come from company CEO.

> **Answer:** 
- ✅ Spoofing

**Another:**

- Fake IP address.
- Also spoofing.

> **Think:** 
- Fake identity.

**On-Path Attack (Man-in-the-Middle)**

- Attacker secretly intercepts communication between two parties.

**Older term:**

- MITM.

**Attacker sits “in the middle.”**


**Can:**


**eavesdrop**

- modify traffic

**Scenario**

- Attacker intercepts login traffic on public Wi-Fi.

> **Answer:** 
- ✅ On-path attack

**Common place:**

- insecure public Wi-fi

**Memory:**

- Attacker on communication path.

**Brute-Force Attack**

- Tries every possible password combination.
- Very slow but systematic.

**Example:**


**aaaa**


**aaab**


**aaac**

- until success.

**Scenario**

- Attacker repeatedly tries all password combinations.

> **Answer:** 
- ✅ Brute-force attack

**Protection:**


**account lockout**


**MFA**

- strong passwords

> **Think:** 
- Force all combinations.

**Dictionary Attack**

- Tries common words/password lists.
- Not every combination.
- Uses dictionary/common passwords.

**Examples:**


**password123**


**admin123**

- qwerty
- Faster than brute force.

**Scenario**

- Attacker uses list of common passwords to crack account.

> **Answer:** 
- ✅ Dictionary attack

**Difference:**


**Brute force:**

- all combinations

**Dictionary:**

- known/common words

**Insider Threat**

- Threat from inside organization.

**Could be:**


**employee**


**contractor**

- admin

**Can be:**


**malicious**

- accidental

**Examples:**


**steals data**


**leaks files**

- deletes systems

**Scenario**

- Disgruntled employee deletes company database.

> **Answer:** 
- ✅ Insider threat

**Another:**

- Employee accidentally leaks confidential data.
- Still insider threat.

> **Think:** 
- Threat comes from trusted insider.

**SQL Injection**

- Attack injects malicious SQL commands into application/database input.

**Targets:**


**login forms**


**search boxes**

- web forms

**Goal:**


**access database**


**modify data**

- bypass authentication
- Example malicious input:
- ' OR '1'='1
- (Not needed to memorize exact syntax for A+, just concept.)

**Scenario**


**Attacker enters malicious code into website login form and gains**

- database access.

> **Answer:** 
- ✅ SQL injection

**Memory:**

- Inject database commands.

**Cross-Site Scripting (XSS)**


**Meaning:**


**Attacker injects malicious script (usually JavaScript) into a trusted**

- website.
- When users visit the page, script runs in their browser.

**Goal:**


**steal cookies/session**


**redirect users**


**show fake forms**

- run malicious scripts

> **Think:** 
- Attack website users through browser.

**How it works (simple)**


**Website has vulnerable input field like:**

- comment box

**search bar**

- forum post
- Attacker inserts script.
- Example idea:
- <script>malicious code</script>
- Then other users load page and script executes.
- (You don’t need to memorize code for A+.)

**Scenario**


**Attacker posts malicious script in website comment section, causing**

- visitors to be redirected to fake login page.

> **Answer:** 
- ✅ Cross-site scripting (XSS)

**Memory:**

- XSS = script injected into website.

> **Think:** 

**X = eXecute script on site**


**(Not official meaning, just memory trick.)**


**Difference from SQL injection:**


**SQL injection → attacks database**

- XSS → attacks browser/users via script
- Very common exam confusion.

**Example:**


**Login form attacks database?**

- ✅ SQL injection

**Comment section runs malicious script?**

- ✅ XSS

**Business Email Compromise (BEC)**

- This is very practical/business-focused.

**Meaning:**


**Attacker impersonates business executive/vendor/employee via email to**

- trick someone into transferring money or sensitive info.
- Usually no malware.
- Just deception.

**Common targets:**


**finance department**


**HR**

- accounting

**Example**


**Fake CEO email:**

- Urgent. Transfer $20,000 to this vendor account immediately.
- Employee thinks it is real.
- Money lost.
- This is BEC.

**Scenario**


**Accounting receives email appearing from CFO requesting urgent wire**

- transfer.

> **Answer:** 
- ✅ Business Email Compromise (BEC)
- Why dangerous:

**trusted identity**


**urgency**

- financial loss

**Memory:**


**BEC =**


**business email scam for money/data**


**Difference from phishing:**


**Phishing:**

- broad attack to many users

**BEC:**

- business-focused financial impersonation attack

**Example:**


**Fake Microsoft password reset email → phishing**


**Fake CEO asks money transfer → BEC**


**Supply Chain / Pipeline Attack**

- Attack targets trusted vendor, software provider, or update pipeline.
- Instead of attacking victim directly, attacker compromises supplier.

> **Think:** 
- Attack something trusted upstream.

**Examples:**


**software updates infected**


**vendor compromised**

- third-party library malware

**Why effective:**

- Victims trust supplier.

**Example**

- Attacker compromises software vendor update server.
- Customers install infected update.
- This is supply chain attack.

**Scenario**


**Company installs legitimate software update containing malware**

- because vendor was compromised.

> **Answer:** 
- ✅ Supply chain attack

**Memory:**


**Supply chain =**


**attack trusted supplier**


**Pipeline attack:**

- Same idea but focuses on software development/deployment pipeline.

**Example:**

  - CI/CD compromise code pipeline compromise
- For A+, treat similarly.

**Vulnerabilities**


**Non-compliant Systems**


**Meaning:**

- System does not follow required rules, standards, or company policies.
- “Compliant” = follows rules.

**Could violate:**

  - security policy

**regulatory requirements**

- company baseline

**Examples:**


**password policy ignored**


**encryption not enabled**

- outdated security settings

**Scenario**


**Company policy requires disk encryption on all laptops, but one laptop**

- has encryption disabled.

> **Issue:** 
- ✅ Non-compliant system
- Because system is not following required policy.

**Another example:**

- Policy requires MFA, but user account has password only.

**Also:**

- ✅ non-compliant

**Memory:**

- Non-compliant = breaks required rules.

**Unpatched Systems**


**Meaning:**

- System missing software/security updates.
- Very common vulnerability.

**Why dangerous:**

- Attackers exploit known vulnerabilities.
- Patch = fix.
- No patch = open door.

**Scenario**


**A Windows server has not installed critical security updates for six**

- months.

> **Issue:** 
- ✅ Unpatched system

**This often leads to:**


**malware infection**


**exploits**

- zero-day after patch release

**Protection:**


**patch management**

- automatic updates

**Memory:**

- No updates = vulnerable.

**Unprotected Systems**

- System missing security protections.

**Examples:**


**no antivirus**


**no firewall**

- security software disabled

**Missing Antivirus**


> **Risk:** 
- malware infection

**ransomware**

- trojans

**Scenario**

- User downloads infected file, but no malware protection installed.

> **Issue:** 
- ✅ unprotected system

**Missing Firewall**


> **Risk:** 

**unauthorized inbound traffic**

- exposed ports

**Scenario**

- PC directly exposed to network without firewall.

> **Issue:** 
- ✅ unprotected system

**Memory:**

- No defense = unprotected.

**EOL (End of Life)**

- Very testable.

**Meaning:**

- Product/vendor no longer supports software/hardware.

**No more:**


**patches**


**updates**

- fixes support

**Danger:**

- Known vulnerabilities remain forever.

**Examples:**


**unsupported OS**

- legacy hardware

**Scenario**


**Company still uses unsupported operating system that no longer**

- receives updates.

> **Issue:** 
- ✅ EOL

**Example:**

- Using old OS after vendor support ended.

**Why dangerous:**


**Often also causes:**


**unpatched system**

- compliance issues

**But BEST answer often:**

- ✅ EOL

**Memory:**

- EOL = dead support.

**Bring Your Own Device (BYOD)**

- Employees use personal devices for work.

**Examples:**

- personal laptop

**personal phone**

- tablet

**Benefits:**


**flexibility**

- convenience

**Risks:**


**weak security**


**mixed personal/work data**

- unmanaged devices

**Security concerns**


**Personal device may:**


**no antivirus**


**no encryption**

- outdated OS

**Scenario**


**Employee accesses company email from personal phone lacking**

- security controls.

**Concern:**

- ✅ BYOD vulnerability

**Company usually manages BYOD with:**


**MDM (mobile device management)**


**policies**

- remote wipe
- Memory:
- BYOD = personal devices at work.

### 2.6 SOHO Malware Removal Procedure


**10-step malware removal process**


#### 1. Identify and Research Malware

- Symptoms Determine what is wrong by recognizing the symptoms (e.g.,

**unusual pop-ups, slow performance, browser redirection, or**


**unexpected security alerts). Research the symptoms to understand**

- what type of malware is being addressed.

#### 2. Quarantine the Infected System


**Immediately disconnect the infected device from the internet (unplug**


**the Ethernet cable and turn off Wi-Fi). This cuts off the malware's**


**communication with its command-and-control server and prevents it**

- from spreading to other computers on the network.

#### 3. Disable System Restore


**Malware frequently hides inside hidden system restore points, meaning**


**a system restore could reintroduce the malware later. Turn off System**

- Restore temporarily in the system settings to delete all previous, potentially infected restore points.

#### 4. Remediate the Infected System


**5. Update Anti-malware Software: Ensure anti-malware and antivirus**

- software definitions are fully updated.

**6. Scan and Removal Techniques: Restart the computer in Safe Mode**

- to prevent the malware from loading automatically upon boot.

**Run a full system scan using your primary antivirus or specialized tools**


**(such as Malwarebytes or built-in Microsoft Defender) to detect and**

- safely quarantine/remove malicious files.

**7. Reimage/Reinstall: Completely reinstall operating system. (If**

  - malware cannot be removed safely)

#### 8. Schedule Scans and Run Updates


**Once the active malware is removed, perform preventative**


**maintenance. Enable automatic definition updates, and schedule**

- regular, automated system scans to ensure your device stays protected.

**9. Enable System Restore and Create a Restore Point**


**Now that the computer is clean and verified, turn System Restore back**


**on. Immediately create a fresh, clean system restore point so that if a**

- problem occurs in the future, you can safely revert to a known, malware-free state.

**10. Educate the End User**


**Address the user's behaviors that led to the infection. Provide education**


**on safe browsing habits, recognizing phishing links, avoiding suspicious**


**email attachments, and the importance of not downloading**

- unauthorized or cracked software.

### 2.7 Workstation Security


**Data-at-Rest Encryption**


**Explanation**

- Protects stored data on a device.

**“Data at rest” means:**


**files saved on disk**


**laptop storage**

- USB storage

**Common tool:**

- BitLocker

**Function**


**Prevents attackers from reading data if device is:**


**stolen**

- lost

**Scenario**

- Employee laptop stolen from car.

**Why company data stays protected?**

- Drive encryption enabled.

**Exam Memory Trick**


**Data at rest = stored data encryption**


**Password Considerations**

- Length: Longer passwords are harder to crack.
- Character Types: Use mixture of: uppercase, lowercase, numbers,

**symbols**

- Uniqueness: Do NOT reuse passwords across accounts.

**Complexity: Complex passwords are harder to guess/brute-force**

- Expiration: Passwords may require periodic changes

**BIOS/UEFI Passwords**


**BIOS / Unified Extensible Firmware Interface passwords protect firmware**

- settings

**Function**

- Adds security before operating system loads.

**Scenario**

- School wants students blocked from booting Linux from USB drives.

**Solution**

- Set BIOS/UEFI password and disable USB boot.
- Exam Memory Trick

**BIOS/UEFI password = pre-boot protection**


**End-User Best Practices**


**Use Screensaver Locks**

- Automatically locks computer after inactivity.

**Log Off When Not in Use**

- Sign out completely when finished using system.

**Secure/Protect Critical Hardware**

- Protect devices physically.

**Secure PII and Passwords**

- PII = Personally Identifiable Information.

**Use Password Managers**

- Password manager securely stores passwords

**Account Management**


**Restrict User Permissions**

- Users should only have permissions needed for their job.

**Called:**

- Least privilege principle

**Function**


**Reduces damage from:**

  - mistakes malware insider threats

**Scenario**


**Office employee cannot install software because using Standard**

- account.
- This is intentional security restriction.

**Exam Memory Trick**


**Least privilege = minimum permissions needed**

- Restrict Log-in Times

**Explanation**

- Controls when users may log in.

**Example:**

- only during office hours

**Function**

- Reduces unauthorized after-hours access.

**Scenario**

- Employee account blocked from logging in after 8 PM.
- Exam Memory Trick

**Time restrictions reduce attack opportunities**

- Disable Guest Account

**Explanation**

- Guest account provides temporary limited access.

**Usually disabled because:**


**unnecessary**

- security risk

**Function**

- Prevents anonymous/temporary access.

**Scenario**


**Technician disables Guest account on company PCs for security**

- hardening.

**Exam Memory Trick**


**Unused accounts should be disabled**

- Use Failed Attempts Lockout

**Explanation**

- Account temporarily locks after too many failed password attempts.

**Example:**

- lock after 5 failed logins

**Function**

- Protects against brute-force attacks.

**Scenario**

- Attacker tries many passwords repeatedly.
- Account becomes locked automatically.

**Exam Memory Trick**


**Lockout stops password guessing**

- Use Timeout/Screen Lock

**Explanation**

- Automatically locks session after inactivity.
- Requires password to continue.

**Function**

- Protects unattended computers.

**Scenario**

- Employee walks away from desk and PC auto-locks after 10 minutes.
- Exam Memory Trick

**Inactive session = auto lock**

- Apply Account Expiration Dates

**Explanation**

- Account automatically expires after certain date.

**Common for:**

  - temporary workers contractors interns

**Function**

- Prevents forgotten active accounts.

**Scenario**

- Contractor account automatically disables after project ends.

**Exam Memory Trick**

- Temporary user = temporary account

**Change Default Administrator Account/Password**


**Explanation**


**Default admin accounts are common attack targets because attackers**

- already know the account name.

**Example:**

- Administrator

**Function**


**Changing:**


**username**

- password makes attacks harder.

**Scenario**

- Company leaves default admin password unchanged on all PCs.
- Attacker easily gains access.

**Best Practice**


**rename admin account**


**use strong unique password**

- avoid default credentials

**Exam Memory Trick**


**Default credentials = major security risk**


**Disable AutoRun**

- AutoRun automatically launches media/software when USB or CD inserted.
- Can spread malware automatically.

**Function**

- Disabling AutoRun prevents automatic execution.

**Scenario**

- Employee inserts infected USB drive.
- If AutoRun enabled:
- malware launches automatically.

**Exam Memory Trick**


**Disable AutoRun = safer USB usage**


**Disable Unused Services**


**Explanation**

- Services running unnecessarily create security risks.

**Unused services may:**


**consume resources**


**open attack paths**

- contain vulnerabilities

**Function**

- Reduce attack surface.

**Scenario**

- Old FTP service still running though company no longer uses it.
- Technician disables service for security hardening.

**Exam Memory Trick**

- Less running services = less attack surface

### 2.8 Mobile Device Security


**Device Encryption**


**Explanation**

- Encrypts stored data on mobile device.
- Protects files if device is:

**lost**

- stolen

**Modern Android and iPhone devices usually support encryption**

- automatically.

**Function**

- Prevents attackers from reading stored data without authentication.

**Scenario**

- Employee loses company phone.
- Because encryption enabled, company data stays protected.

**Screen Locks**

- Facial Recognition : Uses face biometrics to unlock device.

**PIN Codes: Numeric passcode**


**Fingerprint: Uses fingerprint biometrics**


**Pattern: User draws unlock pattern on screen**

- Swipe: Simple swipe unlock with no real authentication.

**Configuration Profiles**


**Explanation**

- Profiles that automatically apply settings to mobile devices.
- Often used in business environments.

**Can configure:**


**Wi-Fi**


**email**


**VPN**

- restrictions security settings

**Function**

- Standardizes and secures company devices.

**Scenario**


**Company issues phones with automatic:**


**VPN setup**


**screen lock policy**

- Wi-Fi configuration
- Using configuration profiles.

**Patch Management**

- “Patch” means update/fix released by vendor.

**OS Updates: Updates operating system security and stability**

- Application Updates: Updates installed applications

**Endpoint Security Software**


**Endpoint = end-user device (laptop, desktop, phone)**


**Antivirus**


**Anti-malware**

- Content Filtering: Blocks dangerous or inappropriate content.

**Locator Applications**


**Explanation**

- Apps/services used to locate lost or stolen devices.

**Examples:**

- Find My iPhone
- Find My Device

**Function**


**Can:**


**track device location**


**play sound**

- lock device remotely

**Scenario**

- Employee loses company phone in restaurant.
- IT uses locator app to find device location.

**Exam Memory Trick**

- Locator app = track missing device

**Remote Wipes**


**Explanation**

- Remotely erase device data.

**Used if device:**


**stolen**


**lost**

- compromised

**Function**

- Protects sensitive company data.

**Scenario**

- Company laptop stolen at airport.
- IT performs remote wipe.

**Exam Memory Trick**


**Remote wipe = erase data remotely**


**Remote Backup Applications**


**Explanation**

- Automatically back up device data to cloud/server.

**Function**


**Protects against:**


**device loss**


**hardware failure**

- accidental deletion

**Scenario**

- Phone damaged but user restores files from cloud backup.

**Exam Memory Trick**


**Backup = recovery protection**


**Failed Log-in Attempts Restrictions**


**Explanation**

- Locks device/account after too many failed attempts.
- Function
- Protects against brute-force attacks.

**Scenario**

- Phone wipes itself after 10 failed unlock attempts.

**Exam Memory Trick**


**Too many failures = lockout/wipe**


**Policies and Procedures**


**MDM (Mobile Device Management): Centralized management system**

- for company mobile devices.

**BYOD: Employee uses personal device for work**

- Corporate-Owned: Company owns and manages device.

**Profile Security Requirements: Security settings applied through**

- profiles.

**Examples:**

  - screen lock required encryption enabled password complexity
  - VPN configuration

### 2.9 Data Destruction and Disposal Methods


**Physical Destruction of Hard Drives**


**Used when drive data must NEVER be recovered**

- Drilling - Physically drill holes through hard drive platters

**Shredding - Machine breaks drive into tiny pieces**

- Degaussing - Uses powerful magnetic field to erase magnetic storage
- Incineration: Burning storage devices completely

**Recycling or Repurposing Best Practices**

- Erasing/Wiping: Overwrites drive data securely.

**Low-Level Formatting: Completely rewrites drive structure at low level**


**Standard Formatting: Quickly prepares drive for use. (User formats USB**

- but forensic software still recovers files.)
  - * Simple deleted and format can use digital forensic (FTK imager,
  - Autospy ) to easy recovery

**Outsourcing Concepts**


**Third-Party Vendor: Company hires outside business to destroy/recycle**


**devices**


**Certification of Destruction/Recycling: Official proof that devices were**

- securely destroyed/recycled.

**Regulatory and Environmental Requirements**


**Explanation**


**Companies must follow laws for:**


**data privacy**

- electronic waste disposal

**Protect:**


**customer data**

- environment

**Scenario**

- Improper disposal leaks customer personal information.
- Company faces legal penalties.

**Exam Memory Trick**

- Security + environmental compliance both matter

### 2.10 SOHO Network Security


**Router settings**


**Change Default Passwords**

  - Default router credentials are publicly known.
  - Prevents attackers from easily accessing router settings

**IP Filtering**


**Allow/block devices based on IP address**


**Usually configured in a router’s firewall settings. You can set rules**


**like "Allow IP address 192.168.1.50 to access the internet, but block**


**192.168.1.55" or "Block all incoming traffic from IP addresses in**

- Country X."

**Firmware Updates**


**Updates router software**


**Content Filtering**

- Blocks unwanted websites/content.
  - Routers with this feature will read your DNS requests (which

**translate website names into numbers) or actively inspect web**


**traffic. When a user tries to load a website, the router checks it**


**against a database (e.g., "Social Media") and drops the connection**

- if it violates set rules

**Physical Placement/Secure Locations**


**Place router securely**


**UPnP (Universal Plug and Play)**

- Allows devices on your network—like gaming consoles, smart TVs,

**and media servers—to automatically discover each other and open**

- router ports (port forwarding).
  - Security risk: If ports are enable, hackers can exploit them to bypass your router's firewall, access your network, or infect connected devices.

**Screened Subnet**

  - DMZ-like isolated network.
  - A demilitarized zone where companies store publicly accessible servers such as a web server

**Configure Secure Management Access**

  - Secure router administration access.
  - HTTPS instead of HTTP strong admin password disable remote admin if unnecessary

**Wireless-Specific Security**

- Changing the service set identifier (SSID): Changing WiFi name
- Disabling SSID broadcast: Hides Wi-Fi name from casual scanning
- Encryption settings: WPA3, WPA2 + AES
- Configure Guest Access: Separate Wi-Fi for visitors
- Firewall Settings
- Disable Unused Ports:

**Explanation**

- Close unnecessary network ports.

**Function**

- Reduces attack surface.

**Scenario**

- Router no longer uses FTP service, so technician closes port 21.

**Exam Memory Trick**

- Unused open ports = security risk
- Port Forwarding/Mapping

**Explanation**

- Redirects internet traffic to internal device.

**Example:**


**gaming server**


**CCTV**

- web server

**Security Risk**

- Opening ports exposes internal systems.

**Scenario**

- User forwards port 3389 for Remote Desktop.
- Creates security risk if poorly secured.

**Exam Memory Trick**

- Port forwarding = controlled exposure

### 2.11 Browser Security Settings


**Browser download/installation**


**Trusted Sources**

  - Only download software/extensions from reliable official sources.
  - Hashing: Hashing verifies file integrity.
  - Window chech Hash: CertUtil -hashfile [FILENAME] SHA256
- Untrusted Sources

**Explanation**


**Avoid downloading from:**

  - random websites pirated software sites unofficial mirrors

**Risks**


**May contain:**

  - malware spyware trojans

**Scenario**

- User downloads “free Photoshop crack” and gets ransomware.

**Exam Memory Trick**

- Cracks/torrents = high malware risk

**Browser patching**


**Explanation**

- Keep browser updated.

**Updates fix:**


**security vulnerabilities**


**bugs**

- exploit weaknesses

**Function**

- Prevents attackers exploiting old browser flaws.

**Scenario**

- Outdated browser exploited by malicious website.
- Updating browser fixes vulnerability.

**Exam Memory Trick**


**Outdated browser = vulnerable browser**


**Extensions and plug-ins**

- Trusted Sources

**Explanation**

- Install extensions only from official extension stores.

**Examples:**

  - Chrome Web Store
  - Firefox Add-ons

**Scenario**

- User installs verified password manager extension from official store.

**Exam Memory Trick**


**Trusted extension source reduces malware risk**

- Untrusted Sources

**Explanation**


**Unofficial extensions may:**

  - steal data inject ads track activity install malware

**Scenario**

- Fake browser extension steals banking credentials.

**Exam Memory Trick**

- Malicious extensions can bypass browser security

**Password managers**


**Explanation**

- Store and manage passwords securely.

**Help users:**


**create strong passwords**


**avoid password reuse**

- autofill credentials safely

**Examples:**


**Bitwarden**


**1Password**

- Google Password Manager

**Scenario**

- User uses same weak password everywhere.
- Technician recommends password manager.

**Exam Memory Trick**


**Password manager = strong unique passwords**


**Secure connections/ sites–valid certificates**


**Secure websites use:**

- HTTPS valid digital certificates

**Certificate proves:**


**website identity**

- encrypted connection

**Signs of secure site**


**padlock icon**

- HTTPS in address bar

**Scenario**


**Browser warns:**


**“Certificate not trusted.”**


**Possible:**


**fake site**


**expired certificate**

- man-in-the-middle attack

**Exam Memory Trick**

- HTTPS + valid certificate = secure connection

**Settings**


**Pop-up Blocker**


**Blocks unwanted pop-up windows**

- Clearing Browsing Data

**Explanation**


**Deletes:**

  - history cookies saved sessions

**Function**

- Improves privacy/security.

**Scenario**

- User clears browsing data before returning shared computer.
- Clearing Cache

**Explanation**

- Deletes temporary stored website files.

**Function**


**Can:**


**fix browser issues**


**remove old site data**

- improve privacy

**Scenario**

- Website displays outdated content until cache cleared.

**Exam Memory Trick**


**Cache = temporary website storage**


**Private-Browsing Mode**


**Examples:**


**Incognito Mode**

- Private Window

**Explanation**


**Browser does not save:**


**history**

- cookies session data locally

**Important Note**

- Does NOT make user anonymous online.
- ISP/network/admin may still see traffic.

**Scenario**

- User logs into account on public PC using private mode.

**Exam Memory Trick**


**Private mode hides local traces, not internet activity**

- Sign-in/Browser Data Synchronization

**Explanation**


**Syncs:**


**bookmarks**


**passwords**


**history**

- settings across devices.

**Security Risk**

- Compromised account may expose synced data.

**Scenario**


**User signs into browser on public PC and accidentally syncs personal**

- passwords.

**Exam Memory Trick**


**Sync = convenience + security consideration**

- Ad Blockers

**Explanation**

- Blocks advertisements and malicious ad networks.

**Function**


**Reduces:**


**tracking**


**malicious ads (malvertising)**

- distractions

**Scenario**

- Ad blocker prevents fake download ads from appearing.

**Exam Memory Trick**


**Ad blockers can improve security**

- Proxy

**Explanation**

- Intermediary server between user and internet.

**Functions**


**Can:**


**filter traffic**

- hide IP

**monitor browsing**

- improve privacy

**Scenario**

- Company routes employee web traffic through proxy server.

**Exam Memory Trick**


**Proxy = middleman server**

- Secure DNS

**Explanation**

- Encrypted DNS requests.

**Examples:**


**DNS over HTTPS (DoH)**

- DNS over TLS (DoT)

**Function**


**Improves:**


**privacy**

- protection from DNS tampering

**Scenario**


**User enables Secure DNS to prevent ISP from seeing DNS queries**

- easily.

**Exam Memory Trick**

- Secure DNS encrypts DNS lookups

**Browser feature management**


**Plug-ins: Extra software components used by browser for special**

- content/features.
- Extensions: Small add-ons that extend browser functionality.
- Features: Built-in browser capabilities/settings

---

## 3.0 Software Troubleshooting


### 3.1 Window OS Troubleshooting

- Blue Screen of Death (BSOD)

**Description**

- BSOD = Windows crashes and shows blue error screen.

**Usually caused by driver issues, hardware failure, or system file**

- corruption.

**Example**

- Install new GPU driver → PC crashes with blue screen.

**Exam Scenario**

- After installing hardware, system shows BSOD during startup.
- Best answer: rollback/update driver or check new hardware.

**Exam Tips / Compare**


**BSOD = system crash**

- Application crash = only one app crashes, Windows still works

**Basic Troubleshooting**


**boot Safe Mode**


**rollback/update drivers**


**check RAM**


**check event logs**

- Repair Windows Files: sfc /scannow

**Degraded performance**


**Explanation**

- Computer becomes slower than normal.

**Common Causes**


**malware**


**low RAM**


**too many startup apps**


**failing HDD**

- overheating

**Scenario**

- PC takes 10 minutes to boot and apps freeze often.

**Troubleshooting**


**Task Manager check**


**malware scan**


**disable startup apps**

- check disk usage

**Exam Memory Trick**


**Slow PC = resource/storage/malware issue**


**Boot issues**


**Explanation**

- System fails to start correctly.

**Common Causes**


**corrupted boot files**


**failed drive**


**OS corruption**

- wrong boot order

**Scenario**

- PC stuck on spinning circle during startup.

**Troubleshooting**


**Startup Repair**


**recovery console**

- check BIOS boot order
- Use command Repair Bootloader bootrec /fixmbr bootrec /fixboot bootrec /rebuildbcd

**Frequent shutdowns**


**Explanation**

- Computer powers off unexpectedly.

**Common Causes**


**overheating**


**failing PSU**


**battery problems**

- thermal protection

**Scenario**

- Laptop shuts down after 15 minutes gaming.

**Likely:**

- Overheating.

**Troubleshooting**

- clean dust

**check fans**

- monitor temperatures

**Applications crashing**


**Explanation**

- Programs close unexpectedly or freeze.

**Common Causes**


**corrupted app**


**incompatible updates**


**low memory**

- bad drivers

**Scenario**

- Browser crashes every time certain website opens.

**Troubleshooting**


**reinstall app**


**clear cache**

- update software

**Low memory warnings**

- Explanation
- System running out of RAM/virtual memory.

**Symptoms**


**freezing**


**slow multitasking**

- warning messages

**Scenario**

- User opens many Chrome tabs and receives low memory warning.

**Troubleshooting**


**close apps**


**increase RAM**

- increase virtual memory

**Exam Memory Trick**


**Low memory = RAM pressure**


**USB controller resource warnings**


**Explanation**

- Too many USB devices drawing power/resources.

**Common Causes**


**overloaded USB hub**


**insufficient power**

- driver conflict

**Scenario**

- External drives disconnect randomly when many USB devices connected.

**Troubleshooting**


**use powered USB hub**


**disconnect unused devices**

- update USB drivers

**System instability**


**Explanation**

- Random freezes/crashes/unpredictable behavior.

**Common Causes**


**overheating**


**bad RAM**

- driver conflicts malware

**Scenario**

- PC freezes randomly without error.

**Troubleshooting**


**memory test**


**update drivers**

- hardware diagnostics

**No OS found**

- Explanation
- System cannot locate operating system.

**Common Causes**


**failed drive**


**disconnected drive**


**corrupted bootloader**

- wrong boot device
- Scenario
- Startup message:
- No operating system found

**Troubleshooting**


**check BIOS boot order**


**verify drive detected**

- repair bootloader

**Exam Memory Trick**


**No OS found = boot device problem**


**Slow profile load**


**Explanation**

- User account/profile loads very slowly.

**Common Causes**


**corrupted profile**


**network profile issue**

- excessive startup scripts

**Scenario**

- Domain user waits 10 minutes at “Loading profile.”

**Troubleshooting**


**check roaming profile**

- create new profile check login scripts

**Time drift**


**Explanation**

- System clock becomes inaccurate over time.

**Common Causes**


**dead CMOS battery**


**NTP sync issue**

- VM timing issue

**Scenario**

- PC loses correct time every reboot.

**Likely:**

- CMOS battery failure.

**Troubleshooting**


**replace CMOS battery**


**sync time server**

- check timezone

**Exam Memory Trick**

- Wrong time after reboot = CMOS battery suspect

### 3.2 Mobile OS & Application Troubleshooting


**Application Fails to Launch**


**Explanation**

- App will not open/start.

**Common Causes**


**corrupted app**


**insufficient storage**


**OS incompatibility**

- app bug

**Scenario**

- User taps banking app but nothing happens.

**Troubleshooting**


**restart phone**


**clear app cache**


**reinstall app**

- update OS/app

**Exam Memory Trick**


**App won’t start → reinstall/update first**


**Application Fails to Close / Crashes**


**Explanation**

- App freezes or closes unexpectedly.

**Common Causes**


**memory issues**


**app bugs**

- corrupted cache outdated app

**Scenario**

- Social media app crashes every few minutes.

**Troubleshooting**


**force stop app**


**clear cache/data**


**update app**

- reboot device

**Application Fails to Update**


**Common Causes**


**no internet**


**low storage**


**incompatible OS**

- app store issue

**Scenario**


**Play Store shows:**

- “Update failed.”

**Troubleshooting**


**check Wi-Fi**


**free storage space**


**restart device**

- update OS

**Exam Memory Trick**


**No storage = update problems**


**Application Fails to Install**


**Common Causes**


**insufficient storage**


**unsupported OS version**


**security restrictions**

- corrupted installer

**Scenario**

- User cannot install app from APK file.

**Troubleshooting**


**verify storage**


**enable install permissions**

- use official app store

**Slow to Respond**


**Explanation**

- Phone/apps become laggy.

**Common Causes**


**low RAM**


**too many background apps**


**malware**

- full storage

**Scenario**

- Phone freezes when switching apps.

**Troubleshooting**


**close apps**


**restart phone**


**clear storage**

- uninstall unused apps

**Exam Memory Trick**


**Full storage = slow phone**


**OS Fails to Update**


**Common Causes**


**low battery**


**insufficient storage**


**network issue**

- unsupported device

**Scenario**

- Android update stuck at 0%.

**Troubleshooting**


**charge device**


**connect stable Wi-Fi**


**free storage**

- reboot device

**Battery Life Issues**


**Common Causes**


**high brightness**


**background apps**


**old battery**

- GPS/Bluetooth always on

**Scenario**

- Battery drains within 2 hours.

**Troubleshooting**


**reduce brightness**


**disable unused radios**


**battery saver mode**

- replace battery

**Exam Memory Trick**


**Background apps drain battery**


**Connectivity Issues**

- Bluetooth Issues

**Common Causes**

  - pairing failure disabled Bluetooth interference

**Troubleshooting**


**re-pair devices**


**toggle Bluetooth off/on**

- remove old pairings
- Wi-Fi Issues

**Common Causes**


**wrong password**


**weak signal**

- DHCP issue

**Troubleshooting**


**forget/reconnect network**


**reboot router**

- check airplane mode

**NFC Issues**

- NFC = Near-Field Communication.

**Used for:**


**tap payments**

- quick pairing

**Common Causes**


**NFC disabled**

- incompatible device
  - poor positioning

**Troubleshooting**

  - enable NFC move devices closer remove thick phone case

**Screen Does Not Autorotate**


**Common Causes**


**rotation lock enabled**


**sensor problem**

- app limitation

**Scenario**

- Phone stays vertical even when rotated.

**Troubleshooting**


**enable auto-rotate**


**reboot device**

- test in another app

**Exam Memory Trick**

- First check rotation lock setting

### 3.3 Mobile OS Security Troubleshooting


**Security concerns**

- Application Source / Unofficial Application Stores

**Explanation**

- Apps installed outside official stores.

**Examples:**


**random APK websites**


**cracked app sites**

- third-party stores

**Security Risks**


**Apps may contain:**


**malware**


**spyware**


**ransomware**

- trojans
- Official stores usually perform security checks.

**Scenario**

- User installs “free premium game APK” from random website.
- Phone becomes infected with spyware.

**Troubleshooting / Solution**


**uninstall suspicious app**


**scan device**

- install apps only from official stores

**Examples:**


**Google Play Store**

- Apple App Store

**Exam Memory Trick**


**Unofficial store = high malware risk**

- Developer Mode

**Explanation**


**Advanced mode used for:**


**debugging**


**USB debugging**

- app testing
- Normally used by developers/technicians.

**Security Risks**


**Can:**


**weaken device security**


**allow unauthorized changes**

- expose device through USB debugging

**Scenario**

- Attacker accesses unlocked phone with USB debugging enabled.

**Troubleshooting / Solution**

- Disable Developer Options when not needed.

**Exam Memory Trick**


**Developer mode increases attack surface**

- Root Access / Jailbreak

**Rooting (Android)**

- Gives full administrator access to Android system.

**Jailbreaking (iPhone)**

- Removes Apple restrictions on iOS.

**Security Risks**


**disables built-in protections**


**allows unauthorized apps**


**increases malware risk**

- may void warranty

**Scenario**


**Rooted Android device infected after installing system-level app from**

- unknown source.

**Troubleshooting / Solution**


**remove root/jailbreak**


**reinstall official OS**

- factory reset if needed

**Exam Memory Trick**


**Android         iPhone**

- Rooting         Jailbreaking

**Both:**

- 👉 reduce security
- Unauthorized / Malicious Applications (Application Spoofing)

**Explanation**

- Fake apps pretending to be legitimate apps.

**Called:**

- Application spoofing.

**Example**


**Fake:**


**banking app**


**WhatsApp clone**

- fake antivirus app designed to steal credentials/data.

**Security Risks**


**credential theft**


**spyware**


**phishing**

- financial theft

**Scenario**

- User installs fake banking app with similar logo/name.
- Attacker steals login credentials.

**Troubleshooting / Solution**


**uninstall app**

- change passwords
  - enable MFA download only verified apps

**Exam Memory Trick**

- Spoofed app = fake trusted app

**Common Mobile Security Symptoms**

- High Network Traffic

**Explanation**

- Phone uses unusually large amount of internet data.

**Possible Causes**

  - malware communicating with attacker background spyware cryptominer cloud sync abuse

**Scenario**

- User notices huge mobile data usage overnight while not using phone.

**Troubleshooting**

  - check data usage by app uninstall suspicious apps scan device disable background data
- Exam Memory Trick

**Unexpected traffic = possible malware activity**

- Degraded Response Time

**Explanation**

- Phone becomes unusually slow.

**Possible Causes**


**malware**


**low storage**


**cryptomining app**

- excessive background apps

**Scenario**


**Phone overheats and becomes extremely laggy after installing unknown**

- APK.

**Troubleshooting**


**remove suspicious apps**


**reboot device**


**free storage**

- malware scan
- Data-Usage Limit Notification

**Explanation**

- Carrier/device warns user about unusually high data usage.
- Possible Causes

**malware traffic**


**spyware uploads**


**background streaming**

- hotspot abuse

**Scenario**

- User receives warning after malicious app secretly uploads data.

**Exam Memory Trick**


**High data use can indicate hidden background activity**

- Limited Internet Connectivity

**Explanation**

- Device connected but internet partially works.

**Possible Causes**


**weak signal**


**DNS issue**


**router issue**


**captive portal**

- IP conflict

**Scenario**

- Wi-Fi connected but apps cannot load properly.

**Troubleshooting**

- reconnect Wi-Fi

**restart router**

- renew IP/reboot phone
- No Internet Connectivity

**Explanation**

- No internet access at all.

**Possible Causes**


**airplane mode**


**Wi-Fi disabled**


**ISP issue**


**wrong password**

- SIM/network issue

**Scenario**

- Phone shows:
- Connected, no internet

**Troubleshooting**


**toggle airplane mode**


**reboot device/router**

- verify network settings
- High Number of Ads

**Explanation**

- Excessive popups/ads appearing unexpectedly.

**Possible Causes**


**adware**


**malicious browser extensions**

- infected apps

**Scenario**

- Ads appear even when no app/browser open.

**Troubleshooting**


**uninstall suspicious apps**


**reset browser**

- malware scan

**Exam Memory Trick**


**Unexpected ads = likely adware**

- Fake Security Warnings

**Explanation**

- Scareware messages pretending device is infected.

**Examples:**


**“YOUR PHONE HAS 5 VIRUSES”**

- “Install cleaner now!”

**Possible Causes**


**malicious websites**

- scareware fake antivirus apps

**Scenario**

- Browser constantly displays fake virus warnings.

**Troubleshooting**


**close browser**


**clear browser data**

- avoid clicking alerts

**Exam Memory Trick**


**Fake urgent warnings = scareware/phishing**

- Unexpected Application Behavior

**Explanation**

- Apps behave abnormally.

**Examples:**


**opening randomly**


**crashing**


**permissions changing**

- sending messages automatically

**Possible Causes**


**malware**


**malicious updates**

- compromised app

**Scenario**

- Messaging app sends spam links automatically.

**Troubleshooting**


**revoke permissions**


**uninstall app**

- update OS
- Leaked Personal Files/Data

**Explanation**

- Sensitive data exposed or stolen.

**Examples:**


**photos leaked**


**passwords stolen**

- contacts exposed

**Possible Causes**


**spyware**


**phishing**


**cloud compromise**

- malicious app permissions

**Scenario**

- User discovers private photos uploaded online without permission.

**Troubleshooting**

- change passwords
  - enable MFA remove malicious apps review cloud accounts

**Exam Memory Trick**

- Unauthorized data exposure = compromise indicator

### 3.4 Personal Computer Security Troubleshooting


**Unable to Access the Network**


**Explanation**

- PC cannot connect to internet/network resources.

**Possible Causes**


**malware changed settings**


**firewall issue**


**disabled adapter**

- DNS/IP issue

**Scenario**


**User infected with malware loses internet access after fake antivirus**

- installation.

**Troubleshooting**


**check IP settings**

- run:
- ipconfig

**disable/re-enable adapter**

- malware scan

**Exam Memory Trick**


**No network = check adapter/IP/malware**


**Desktop Alerts**


**Explanation**

- Unexpected warnings/messages appear on desktop.

**Possible Causes**


**scareware**


**malware**

- fake antivirus

**Scenario**

- Popup repeatedly says:
- Your PC is infected! Click here now!

**Troubleshooting**


**do NOT click popup**


**disconnect internet**

- run anti-malware scan

**Exam Memory Trick**

- Aggressive alerts = likely scareware

**False Alerts Regarding Antivirus Protection**


**Explanation**


**Fake messages claim antivirus:**


**expired**


**disabled**

- infected when not true.

**Possible Causes**


**rogue antivirus**

- malware

**Scenario**

- Fake “security center” asks for payment to remove fake threats.

**Troubleshooting**


**verify real antivirus status**


**uninstall rogue software**

- malware removal

**Exam Memory Trick**


**Fake AV warnings = rogue antivirus**


**Altered System or Personal Files**

- Missing/Renamed Files
- Explanation
- Files disappear or names/extensions change.

**Possible Causes**


**ransomware**


**malware**

- accidental deletion

**Scenario**

- Documents renamed:
- report.docx.locked
- Likely ransomware.

**Troubleshooting**


**disconnect network**


**scan system**

- restore from backup

**Inability to Access Files**

- Files cannot open/access.

**Possible Causes**


**encryption by ransomware**


**permission changes**

- corruption
- Scenario
- User receives ransom note after files become inaccessible.

**Exam Memory Trick**

- Encrypted inaccessible files = ransomware

**Unwanted Notifications within the OS**


**Explanation**

- Unexpected notifications constantly appear.

**Possible Causes**


**adware**


**malicious browser notifications**

- bundled software

**Scenario**

- Windows repeatedly shows gambling ads in notification area.

**Troubleshooting**


**disable browser notifications**

- remove suspicious apps/extensions

**OS Update Failures**


**Explanation**

- Windows updates fail repeatedly.

**Possible Causes**

- corrupted update files
  - malware insufficient storage broken services

**Scenario**

- Windows Update stuck at:
- 0%

**Troubleshooting**

  - restart Windows Update service free storage run:
- sfc /scannow

**Random/Frequent Pop-ups**


**Explanation**

- Browser constantly opens unwanted ads/windows.

**Possible Causes**

  - adware malicious extensions infected websites
- Scenario
- Ads appear even without browsing.

**Troubleshooting**


**remove extensions**


**reset browser**

- malware scan

**Exam Memory Trick**


**Excessive popups = adware**


**Certificate Warnings**

- Browser warns about invalid HTTPS certificates.

**Possible Causes**


**fake site**


**expired certificate**


**MITM attack**

- wrong system date/time

**Scenario**

- Browser shows:
- NET::ERR_CERT_DATE_INVALID

**Troubleshooting**


**verify system time**


**avoid unsafe website**

- check certificate validity

**Exam Memory Trick**


**Certificate warning = trust/security issue**


**Redirection**


**Explanation**

- Browser redirects user to unexpected websites.

**Possible Causes**


**browser hijacker**


**malicious extension**

- DNS malware
- Scenario
- Searching Google redirects to fake shopping pages.

**Troubleshooting**


**remove suspicious extensions**


**reset browser**

- flush DNS:
- ipconfig /flushdns

**Exam Memory Trick**


**Unexpected redirects = browser hijacking**


**Degraded Browser Performance**


**Explanation**

- Browser becomes slow/freezes frequently.

**Possible Causes**


**too many extensions**


**malware**


**cache overload**

- insufficient RAM

**Scenario**

- Browser takes 30 seconds to open tabs.

**Troubleshooting**

- clear cache

**disable extensions**

- malware scan

---

## 4.0 Operation Procedures


### 4.1 Implement best practices associated with

documentation and support systems information
management

**Ticketing Systems**

- User Information

**Explanation**

- Information about person reporting issue.

**Usually includes:**

  - name department contact info employee ID

**Purpose**


**Helps technician:**

  - identify user contact user track issue ownership
- Device Information

**Explanation**

- Information about affected device.

**Examples:**


**PC name**


**IP address**


**operating system**

- serial number

**Purpose**

- Helps troubleshoot specific system.
- Description of Issues

**Explanation**

- Clear explanation of problem symptoms.

**Should include:**


**what happened**


**when it happened**

- error messages
- Categories

**Explanation**

- Classifies ticket type.

**Examples:**


**hardware**


**software**


**network**


**security**

- printer

**Purpose**

- Routes ticket to correct technician/team.
- Severity (Task Priority)

**Explanation**

- Measures impact/urgency.

**Example Levels**

  - Severity       Meaning
  - Minor
  - Low inconvenience
  - Medium         User impacted
  - Business
  - High affected
  - Critical       Major outage
- Escalation Levels

**Explanation**

- Higher-level technicians handle more complex issues.

**Example**

  - Level          Role
  - Tier 1         Basic help desk
  - Tier 2         Advanced support
  - Tier 3         Specialists/enginee
- Clear, Concise Written Communication
  - Issue Description (Example: User unable to connect to Wi-Fi after password reset.)
  - Progress Notes (Example: Rebooted router and renewed IP address.
  - Issue persists.)
  - Issue Resolution (Example: Updated wireless driver resolved connectivity issue.)

**Asset Management**

- Inventory Lists

**Explanation**

- List/database of company assets.

**Includes:**

  - device name serial number assigned user location

**Purpose**

- Helps track equipment and prevent loss.
- Configuration Management Database (CMDB)

**Explanation**


**Detailed IT environment database**


**Central database storing:**

  - asset details configurations relationships between systems
- More advanced than simple inventory list.

**Contains**


**hardware info**


**software versions**


**network relationships**

- change history
- Asset Tags and IDs

**Explanation**

- Unique identifiers attached to devices.
- Usually sticker/barcode.

**Purpose**

- Quick identification and tracking.
- Procurement Life Cycle

**Explanation**

- Full life cycle of company equipment.

**Stages**


**Stage           Meaning**


**Procurement     Purchase device**


**Deployment      Give to user**


**Maintenance     Support/repair**

- Retirement      Dispose/recycle
- Warranty and Licensing
- Explanation
- Manufacturer support/repair coverage.

**Scenario**

- Laptop repaired free because still under warranty.

**Term              Meaning**


**Warranty          Hardware coverage**

- License           Software permission
- Assigned Users

**Explanation**

- Records which employee uses which device.

**Purpose**


**Helps:**

  - accountability troubleshooting device recovery

**Types of IT Support Documents**

- Incident Reports

**Explanation**


**Document describing:**

  - security incident outage unusual event

**Includes:**

  - what happened

**time/date**


**affected systems**

- actions taken

**Standard Operating Procedures (SOPs)**


**Step-by-step instructions for routine tasks**


**Software Package Custom Installation Procedure**

  - Instructions for installing company-specific software setup.
- New User / Onboarding Setup Checklist

**Explanation**

- Checklist for preparing new employee accounts/devices.

**May Include**


**create user account**


**assign laptop**


**email setup**


**permissions**

- MFA setup
- User Off-boarding Checklist

**Explanation**

- Checklist used when employee leaves company.

**May Include**


**disable accounts**

- collect devices

**revoke VPN access**

- transfer files/email

**Scenario**

- Employee resigns.
- IT disables badge access and Office 365 account immediately.

**Exam Memory Trick**


**Off-boarding = removing access**

- Service-Level Agreements (SLAs)

> 💡 **Key Tip:** Agreement defining support expectations Includes: response time uptime resolution targets


**Internal SLA**

- Agreement within company departments.

**Scenario**


**IT promises employees:**

  - password reset within 30 minutes

**External / Third-Party SLA**

- Agreement with outside vendor/provider.
- Scenario
  - Internet provider guarantees:
  - 99.9% uptime
  - Exam Memory Trick
  - SLA = promised service expectations

### 4.2 Change management procedures.

- Documented Business Processes

> 💡 **Key Tip:** Changes should follow official documented procedures.

- Rollback Plan

**Explanation**

- Plan to undo change if something fails.

**Also called:**

- backout plan.

**Purpose**

- Restore system quickly after failed change.

**Scenario**

- Windows update causes accounting software failure.

**Rollback plan:**

  - uninstall update restore previous configuration

**Exam Memory Trick**


**Rollback = return to previous working state**

- Backup Plan

**Explanation**

- Create backup BEFORE making changes.

**May include:**


**files**


**system image**


**database backup**

- configuration backup

**Purpose**


**Protects against:**


**data loss**


**failed updates**

- corruption

**Scenario**

- Technician backs up server before firmware upgrade.

**Exam Memory Trick**


**Backup BEFORE change**

- Sandbox Testing

**Explanation**

- Testing changes in isolated environment first.

**Sandbox:**


**separate test environment**

- does not affect production systems

**Purpose**

- Detect problems safely before deployment.

**Scenario**


**IT tests Windows patches in virtual machine before deploying company-**

- wide.

**Exam Memory Trick**


**Sandbox = safe testing area**

- Responsible Staff Members

**Explanation**


**Clearly define who is responsible for:**


**approving**


**implementing**


**testing**

- documenting changes

**Purpose**

- Avoids confusion and accountability problems.

**Scenario**

- Network engineer assigned responsibility for firewall update.

**Exam Memory Trick**

- Everyone should know their role
- Change Management

> 💡 **Key Tip:** Maximizes the number of successful IT changes

- Request Forms

**Explanation**

- Official form used to request change.

**Contains:**

  - what changes why needed systems affected approval info

**Scenario**

- Technician submits request before changing firewall rules.

**Exam Memory Trick**


**No request = unauthorized change**

- Purpose of the Change

**Explanation**

- Reason why change is needed.

**Examples:**

  - security patch

**performance improvement**

- bug fix

**Scenario**

- Purpose:
- Upgrade VPN server to fix security vulnerability.

**Exam Memory Trick**


**Every change needs business reason**

- Scope of the Change

**Explanation**


**Defines:**


**what systems/users affected**

- how large change is

**Scenario**

- Windows update applied only to Finance department PCs.

**Exam Memory Trick**


**Scope = how far change affects environment**


**Change Type**

- Standard Change

**Explanation**

- Low-risk, routine, preapproved change.

**Examples:**


**password reset**

- scheduled updates

**Scenario**

- Monthly antivirus update deployment.

**Exam Memory Trick**


**Standard = routine and approved already**

- Normal Change

**Explanation**

- Regular planned change requiring review/approval.

**Scenario**

- Upgrading company email server.

**Exam Memory Trick**


**Normal = planned change needing approval**

- Emergency Change

**Explanation**

- Urgent change requiring immediate action.
- Usually security/outage related.

**Scenario**

- Critical ransomware vulnerability patched immediately.

**Exam Memory Trick**

- Emergency = act fast to reduce damage
- Date and Time of Change (Change schedule)

> 💡 **Key Tip:** Change schedule: Helps plan the changes and assists in communicating such changes to the stakeholders to avoid conflicts

- Change Freeze

**Explanation**

- Period where changes are NOT allowed.

**Usually during:**

  - holidays major business periods critical operations

**Scenario**

- Retail company freezes changes during Black Friday sales week.
- Exam Memory Trick

**Change freeze = no risky changes allowed**

- Maintenance Windows

**Explanation**

- Approved time period for changes/maintenance.

**Usually:**

  - nights weekends

**Scenario**

- Server updates scheduled Sunday 2 AM.

**Exam Memory Trick**

- Maintenance window = safest time for changes
- Affected Systems / Impact

**Explanation**


**Identify:**


**devices**


**servers**


**users**

- services affected

**Scenario**

- Network switch replacement affects 3 office floors.
- Exam Memory Trick

**Know what breaks if change fails**


**Risk Analysis**

- Evaluate possible risks before change.

**Risk Level**


**Examples:**

  - low medium high

**Scenario**


**Core firewall replacement marked high risk due to possible network**

- outage.

**Exam Memory Trick**

- Higher impact = higher risk

**Change Board Approvals**


**Also called:**

- CAB (Change Advisory Board).

**Explanation**

- Group reviews and approves major changes.

**Purpose**


**Ensures:**


**proper planning**

- reduced business risk

**Scenario**

- CAB approves datacenter migration project.

**Exam Memory Trick**


**CAB approves important changes**

- Implementation

**Explanation**

- Actual deployment of change.

**Must follow:**


**approved plan**

- documented steps

**Scenario**


**Technician installs approved firmware update during maintenance**

- window.
- Peer Review

**Explanation**

- Another technician reviews plan/configuration.

**Purpose:**


**catch mistakes**

- improve accuracy

**Scenario**

- Second admin reviews firewall rules before deployment.

**Exam Memory Trick**


**Second pair of eyes reduces errors**

- End-User Acceptance

**xplanation**

- Users verify system works correctly after change.

**Scenario**

- Employees confirm payroll software works after server migration.

**Exam Memory Trick**

- Change not complete until users confirm success

### 4.3 Workstation Backup & Recovery


**Backup Types**

- Full Backup

**Explanation**

- Backs up ALL selected data every time.

**Advantages**

  - easiest recovery complete copy

**Disadvantages**

  - slow large storage usage

**Scenario**

- Company performs full backup every Sunday night.

**Exam Memory Trick**


**Full = everything**

- Incremental Backup

**Explanation**

- Backs up ONLY changes since last backup.
- (last full OR incremental)

**Advantages**


**fast**

- small storage use

**Disadvantages**


**Recovery requires:**


**last full backup**

- ALL incrementals

**Scenario**


**Monday full backup**


**Tuesday incremental = Tuesday changes only**

- Wednesday incremental = Wednesday changes only

**Exam Memory Trick**

- Incremental = smallest/fastest
- Differential Backup

**Explanation**

- Backs up changes since LAST FULL backup.

**Advantages**

- Recovery easier than incremental.

**Disadvantages**

- Gets larger every day until next full backup.

**Scenario**


**Sunday full backup**


**Monday differential = Monday changes**

- Tuesday differential = Monday + Tuesday changes

**Exam Memory Trick**


**Differential grows daily**

- Synthetic Full Backup

**Explanation**


**Creates “new full backup” using:**


**previous full backup**

- incrementals
- WITHOUT re-copying all original data again.

**Advantages**

- saves time
  - reduces network traffic

**Scenario**

- Backup server combines incrementals into synthetic full automatically.

**Exam Memory Trick**

- Synthetic full = virtual rebuilt full backup

**Recovery Methods**

- In-place / Overwrite Recovery

**Explanation**

- Restore data back to original location.
- Existing files may be overwritten.

**Scenario**

- Deleted spreadsheet restored to original Documents folder.

**Exam Memory Trick**


**In-place = original location**

- Alternative Location Recovery

**Explanation**

- Restore data to different location.

**Useful for:**

  - testing avoiding overwrite comparison

**Scenario**

- Technician restores backup to external drive for investigation.

**Exam Memory Trick**

- Alternative = restore somewhere else

**Backup Testing**


**Explanation**

- Verify backups actually work.
- Very important.

**Frequency**


**Testing should occur:**


**regularly**


**after major changes**

- according to policy

**Scenario**

- Company performs monthly restore tests.

**Exam Memory Trick**


**Untested backup = unreliable backup**


**Backup Rotation Schemes**

- Onsite Backup

**Explanation**

- Backup stored locally.

**Examples:**

  - NAS local server external drive

**Advantages**

  - fast recovery

**Risks**

  - fire theft ransomware
- Offsite Backup

**Explanation**

- Backup stored at different location/cloud.

**Advantages**

- Protects against physical disasters.

**Scenario**

- Office burns down but cloud backup survives.
- Exam Memory Trick

**Type               Benefit**


**Onsite             Faster restore**

- Offsite            Disaster protection
- Grandfather-Father-Son (GFS)

**Explanation**


**Backup rotation system using:**


**daily**


**weekly**

- monthly backups

**Structure**


**Level          Meaning**


**Son            Daily**


**Father         Weekly**

- Grandfather    Monthly

**Scenario**


**Daily backups kept 7 days, weekly backups kept 1 month, monthly**

- backups kept 1 year.

**Exam Memory Trick**


**GFS = daily, weekly, monthly rotation**


**3-2-1 Backup Rule**


**Keep:**


**3 copies of data**


**2 different storage types**

- 1 copy offsite
- Example

**Copy               Location**


**Original           PC**


**Backup 1           NAS**

- Backup 2           Cloud storage

**Purpose**


**Protects against:**

  - hardware failure ransomware disasters

**Exam Memory Trick**

- 3 copies, 2 media, 1 offsite

### 4.4 Common Safety Procedures

- Electrostatic Discharge (ESD) Strap
- Explanation
- Wrist strap preventing static electricity damage.

**Connected to:**


**grounded surface**

- ESD mat

**Purpose**


**Protects sensitive components:**


**RAM**


**CPU**

- motherboard

**Scenario**

- Technician wears ESD strap while installing RAM.

**Exam Memory Trick**


**ESD strap = protects components from static**

- ESD Mats

**Explanation**

- Antistatic work surface.
- Used when repairing computers.

**Purpose**

- Safely dissipates static electricity.

**Scenario**

- Motherboard placed on ESD mat during repair.

**Exam Memory Trick**


**Mat protects devices on workspace**

- Electrical Safety (Equipment grounding )

**Explanation**

- Proper grounding prevents electrical shock and damage.

**Purpose**


**Protect:**


**technician**

- equipment

**Scenario**

- Technician verifies PSU properly grounded before servicing workstation.

**Exam Memory Trick**


**Grounding prevents shock and damage**


**Proper Component Handling and Storage**


**Explanation**


**Handle components carefully to avoid:**


**static damage**


**physical damage**

- contamination

**Best Practices**


**hold cards by edges**


**avoid touching contacts/chips**

- store safely
- Scenario
- Technician handles CPU by edges instead of touching pins.

**Exam Memory Trick**


**Touch edges, not contacts**

- Antistatic Bags

**Explanation**

- Special bags protecting components from static electricity.
- Usually silver or pink bags.

**Used For**


**RAM**


**GPUs**

- motherboards

**Scenario**

- Technician stores replacement motherboard in antistatic bag.

**Exam Memory Trick**


**Antistatic bags protect during storage/transport**


**Compliance with Government Regulations**

- Explanation
- Follow legal safety/environment rules.

**Examples:**


**disposal laws**


**workplace safety**

- hazardous material handling

**Scenario**

- Company follows e-waste disposal regulations for old batteries.

**Exam Memory Trick**


**Follow legal and environmental rules**


**Personal Safety**

- Disconnect Power Before Repairing PC

**Explanation**

- Always unplug power before opening system.

**Purpose**


**Prevent:**

  - electric shock short circuits hardware damage

**Scenario**

- Technician disconnects laptop battery before replacing SSD.
- Lifting Techniques

**xplanation**

- Lift heavy equipment safely.

**Best Practices**


**bend knees**


**keep back straight**

- lift with legs

**Scenario**

- Technician uses proper lifting when moving UPS battery.

**Exam Memory Trick**


**Lift with legs, not back**

- Fire Safety

**Explanation**

- Know proper fire prevention and extinguisher use.

**Important**


**Electrical fires:**

- ❌ do NOT use water

**Use:**

- Class C extinguisher

**Scenario**

- Power supply catches fire; technician uses Class C extinguisher.

**Exam Memory Trick**


**Electrical fire = Class C extinguisher**

- Safety Goggles

**Explanation**


**Protect eyes from:**


**debris**


**sparks**

- chemicals

**Scenario**

- Technician wears goggles while drilling damaged hard drive.
- Air Filter Mask

**Explanation**


**Protects from:**

  - dust smoke particles

**Scenario**

- Technician cleans dusty server room using air filter mask.

**Exam Memory Trick**

- Mask protects lungs from particles

### 4.5 Environmental Impacts & Local Environment

Controls
- MSDS Documentation

> 💡 **Key Tip:** MSDS = Material Safety Data Sheet (now often called SDS)

- Proper Battery Disposal

**Explanation**

- Batteries contain hazardous chemicals.
- Should NOT be thrown in regular trash.

**Proper Disposal**


**recycling center**

- approved e-waste disposal

**Scenario**

- IT department recycles swollen laptop batteries properly.

**Exam Memory Trick**


**Batteries = hazardous waste**

- Proper Toner Disposal

**Explanation**


**Printer toner can:**


**contaminate environment**

- irritate lungs

**Best Practice**


**Use:**


**recycling programs**

- approved disposal methods

**Scenario**


**Technician returns used toner cartridges to manufacturer recycling**

- program.
- Proper Disposal of Other Devices and Assets
- Explanation
- Old electronics require proper disposal.

**Examples:**


**PCs**


**monitors**

- drives

**Important**

- Securely wipe data before disposal.

**Scenario**

- Company shreds failed hard drives before recycling PCs.

**Exam Memory Trick**

- Dispose safely AND protect data
- Temperature, humidity-level awareness, and proper ventilation

> 💡 **Key Tip:** Condition       Risk Low humidity    Static High humidity   Moisture damage

- Location / Equipment Placement

**Explanation**

- Place equipment safely.

**Avoid:**

- heat sources

**direct sunlight**


**wet areas**

- blocked vents

**Scenario**

- Printer moved away from heater vent to prevent overheating.
- Dust Cleanup

**Explanation**

- Dust blocks airflow and causes overheating.

**Risks**


**fan failure**


**overheating**

- electrical problems

**Scenario**

- Dust buildup causes PC fan noise and high temperatures.
- Compressed Air / Vacuums

**Compressed Air**


**Explanation**

- Used to blow dust from equipment safely.

**Best Practice**

- Short bursts while holding fan blades still.

**Vacuums**


**Explanation**

- Special ESD-safe vacuums used for electronics.
- Regular vacuums may generate static.

**Exam Memory Trick**

- Use ESD-safe cleaning methods

**Power surges, brownouts, and blackouts**

- UPS (Uninterruptible Power Supply)

**Explanation**

- Battery backup providing temporary power.

**Functions**

  - keeps devices running briefly allows safe shutdown protects from brownouts/blackouts

**Scenario**

- UPS keeps server online during short outage.
- Surge Suppressor

**Explanation**

- Protects against voltage spikes/surges.

**Important**

- Does NOT provide battery backup.

**Scenario**

- Gaming PC plugged into surge protector during thunderstorm.

**Exam Memory Trick**


**Device            Protects Against**


**UPS               Blackouts + brownouts**

- Surge suppressor Voltage spikes only

### 4.6 Importance of prohibited content/activity and

privacy, licensing, and policy concepts

**Incident Response**

- Chain of Custody

**Explanation**


**Documentation showing:**

  - who handled evidence when where what happened to it
- Used to preserve evidence integrity.

**Important for:**

  - legal investigations digital forensics

**Scenario**


**Technician collects infected hard drive and records:**

  - date/time

**person handling drive**

- transfer history

**Exam Memory Trick**


**Chain of custody = evidence tracking log**

- Informing Management / Law Enforcement

**Explanation**


**Serious incidents may require notifying:**


**management**


**security team**


**legal department**

- law enforcement

**When Necessary**


**Examples:**


**ransomware**


**data breach**

- stolen company data

**Scenario**

- Company reports large customer data breach to authorities.

**Exam Memory Trick**


**Major incidents may require escalation outside IT**

- Copy of Drive (Data Integrity & Preservation)

**Explanation**

- Create forensic image/copy of drive before analysis.
- Technicians should NOT work on original evidence directly.

**Purpose**


**Preserve:**


**original evidence**


**metadata**

- integrity

**Scenario**

- Forensic analyst creates bit-by-bit image of compromised laptop drive.

**Exam Memory Trick**

- Analyze copy, preserve original

**Data Integrity**


**Means:**

- data remains unchanged and trustworthy.

**Preservation**


**Means:**

- protect evidence from modification/damage.
- Incident Documentation
- Explanation
- Document everything during incident.

**Includes:**


**timeline**


**symptoms**


**actions taken**


**affected systems**

- evidence collected

**Purpose**


**accountability**


**troubleshooting**


**legal evidence**

- future prevention

**Scenario**


**Security team documents ransomware infection process and**

- containment steps.

**Exam Memory Trick**


**If not documented, it didn’t happen**

- Order of Volatility
- Explanation
- Collect MOST temporary/volatile data FIRST before it disappears.

**General Order**


**Most Volatile       Least Volatile**


**CPU cache/registers Archived backups**


**RAM                 Hard drives**

- Running processes   Optical media/logs

**Why Important?**

- RAM data disappears after shutdown.
- Scenario
- Technician captures RAM contents before powering off infected server.

**Exam Memory Trick**

- Collect temporary data first

**Simple Volatility Order Memory**

- RAM before disk

**because:**


**RAM disappears quickly**

- disk data remains longer
- Licensing/digital rights management (DRM)/ end-user license agreement (EULA)
- Valid Licenses

**Explanation**

- Software must be legally licensed before use.

**Examples**


**purchased Windows key**


**Microsoft 365 subscription**

- enterprise software license

**Scenario**

- Company fined for using unauthorized copies of software.
- Exam Memory Trick

**Valid license = legal software use**

- Perpetual License Agreement

**Explanation**

- One-time purchase license.
- User can use software permanently for that version.

**Example**


**Older Microsoft Office versions:**


**buy once**

- use forever
- (no subscription)

**Scenario**

- Company buys CAD software with perpetual license.

**Exam Memory Trick**


**Perpetual = pay once, own indefinitely**

- Personal-Use License vs Corporate-Use License

**Personal-Use License**


**Explanation**

- License intended for individual/home use only.
- Usually cheaper.
- Restrictions
- Cannot legally use in business environment.

**Corporate-Use License**


**Explanation**

- Business/enterprise license for organizations.

**Often includes:**


**centralized management**


**multiple users/devices**

- commercial rights

**Scenario**

- Employee installs home-use software on company PCs illegally.

**Exam Memory Trick**


**License          Intended Use**


**Personal         Individual/home**

- Corporate        Business/company
- Open-Source License

**Explanation**

- Software source code publicly available.

**Users may:**


**view**


**modify**

- redistribute depending on license type.

**Examples**


**Linux Kernel**


**Mozilla Firefox**

- LibreOffice

**Advantages**


**free/flexible**


**community-driven**

- customizable

**Scenario**

- Company uses Linux server to reduce licensing costs.

**Exam Memory Trick**


**Open source = visible/editable source code**

- DRM (Digital Rights Management)

**Explanation**

- Technology controlling access/copying of digital content.

**Used to prevent:**


**piracy**

- unauthorized sharing

**Examples**


**streaming restrictions**

- game activation movie copy protection

**Scenario**

- Downloaded movie cannot be copied due to DRM restrictions.

**Exam Memory Trick**

- DRM protects digital content ownership
- EULA (End-User License Agreement)

**Explanation**

- Legal agreement between software vendor and user.

**Defines:**


**allowed usage**


**restrictions**

- responsibilities
- Usually shown during installation.

**Scenario**

- User clicks:
- I Agree during software installation.

**Exam Memory Trick**

- EULA = software usage rules
- Non-disclosure agreement (NDA)/mutual non-disclosure agreement (MNDA)
- NDA (Non-Disclosure Agreement)

**Explanation**

- Legal agreement preventing sharing confidential information.

**Used For**


**employees**


**contractors**

- vendors

**Scenario**

- IT contractor signs NDA before accessing company network.

**Exam Memory Trick**


**NDA = keep secrets confidential**

- MNDA (Mutual Non-Disclosure Agreement)

**Explanation**

- Both parties agree to protect confidential information.

**Difference from NDA**


**Agreement       Protection Applies To**


**NDA             One side**

- MNDA            Both sides

**Scenario**

- Two companies discuss partnership and both protect shared secrets.

**Exam Memory Trick**

- M in MNDA = mutual/both sides
- Regulated Data

> 💡 **Key Tip:** Regulated data = sensitive information protected by: laws regulations company policies


**Credit Card Payment Information**


**Explanation**

- Payment card information used in financial transactions.

**Examples:**

  - card number
  - CVV expiration date

**Regulations**


**Protected by:**

  - PCI-DSS (Payment Card Industry Data Security Standard)

**Scenario**


**Retail company stores customer card numbers insecurely and suffers**

- data breach.

**Best Practices**


**encrypt payment data**


**restrict access**

- never store unnecessary card data

**Exam Memory Trick**


**Credit card data → PCI-DSS**


**Personal Government-Issued Information**


**Explanation**

- Government-issued identification information.

**Examples:**


**passport number**


**driver license number**

- national ID number

**Risks**

- Identity theft if leaked.

**Scenario**

- HR database containing passport scans gets compromised.

**Best Practices**


**encrypt records**


**limit employee access**

- secure storage

**Exam Memory Trick**


**Government IDs = highly sensitive**


**PII (Personally Identifiable Information)**


**Explanation**

- Information that can identify a person.

**Examples**


**full name**


**address**


**phone number**


**email**

- social security/national ID number

**Risks**


**identity theft**


**phishing**

- fraud

**Scenario**

- Employee accidentally emails customer PII to wrong recipient.

**Best Practices**


**least privilege access**


**encryption**

- secure disposal

**Exam Memory Trick**


**PII = identifies individual person**


**Healthcare Data**

- Personal health information (PHI)

**Explanation**

- Medical/health-related information.

**Examples:**


**medical records**


**diagnoses**


**prescriptions**

- insurance information

**Regulations**


**In U.S.:**

- HIPAA

**Scenario**

- Hospital employee improperly accesses patient medical records.

**Best Practices**


**strong access controls**


**encryption**

- audit logging

**Exam Memory Trick**

- Healthcare data → HIPAA

**Data Retention Requirements**


**Explanation**


**Rules defining:**

  - how long data must be kept when it must be deleted

**Purpose**

  - legal compliance auditing business requirements

**Scenario**

- Company required to keep tax records for 7 years.

**Risks**


**Keeping data too long:**

  - increases breach risk

**Deleting too early:**

  - violates regulations

**Exam Memory Trick**

- Retention = how long data is stored

**Acceptable Use Policy (AUP)**


**Explanation**

- AUP = rules describing how users may properly use company IT resources.

**Covers:**


**computers**


**internet**


**email**


**network**

- devices
- Users usually must read and agree to it.

**Purpose**


**Protects:**


**company systems**


**data**


**employees**

- legal compliance

**Common AUP Rules**


**Users should NOT:**


**install unauthorized software**


**visit illegal/inappropriate websites**


**share passwords**

- misuse company resources

**Scenario**

- Employee downloads pirated software on company laptop, violating AUP.
- Exam Memory Trick

**AUP = acceptable behavior rules**


**Regulatory and Business Compliance Requirements**


**Explanation**


**Splash screen = Message shown before log-in**


**A splash screen can help organizations meet:**


**legal requirements**


**security policies**

- compliance standards before users access systems.

**Purpose of Compliance Splash Screens**


**The splash screen:**


**warns unauthorized users**


**informs activity is monitored**


**reminds users of company policies**

- supports legal enforcement

**Common Compliance Message**

- Authorized users only.
- All activity may be monitored and recorded.
- Unauthorized access is prohibited.

**Why Important?**

- Helps organizations comply with:

**security regulations**


**audit requirements**

- internal security policies

**Scenario**


**Hospital employees see splash screen before accessing patient records to**

- support HIPAA compliance.

**Business Compliance Example**


**Bank systems display warning banner to:**


**protect financial data**


**meet regulatory requirements**

- provide legal notice

**Exam Memory Trick**

- Splash screen = legal/security warning before login

### 4.7 Communication techniques and

professionalism.
- Professional Appearance & Appropriate Attire
- Formal Attire

**Explanation**

- Professional business clothing.

**Usually includes:**


**suit**


**tie**


**dress shoes**

- formal dress/business wear

**Used In**

- executive meetings

**corporate presentations**

- high-level business environments

**Scenario**

- IT consultant meeting company executives wears formal attire.
- Business Casual

**Explanation**

- Professional but less formal.

**Examples:**


**collared shirt**


**polo shirt**


**slacks**

- neat shoes

**Usually:**

- ❌ no ripped jeans
- ❌ no graphic T-shirts

**Used In**


**normal office IT support**


**help desk**

- business offices

**Scenario**

- Help desk technician wears polo shirt and khakis in office environment.

**Exam Memory Trick**

- Business casual = professional but comfortable

**Important Professionalism Tips**


**Maintain Clean Appearance**


**clean clothes**


**good hygiene**

- organized appearance

**Consider Safety**


**In hardware environments:**


**avoid loose jewelry**

- avoid loose clothing near equipment

**Customer-Facing Environments**


**Technicians should appear:**

  - trustworthy respectful professional

**Use proper language and avoid jargon, acronyms, and slang, when**

- applicable.
- Maintain a positive attitude/ project confidence.
- Actively listen and avoid interrupting the customer.
- Be culturally sensitive.
- Use appropriate professional titles and designations, when applicable.
- Be on time (if late, contact the customer).

**Avoid distractions**


**Personal calls**


**Texting/social media sites**

- Personal interruptions

**Appropriately deal with difficult customers or situations**

- Do not argue with customer and/or be defensive.
- Avoid dismissing customer issues.
- Avoid being judgmental.

**Clarify customer statements (i.e., ask open-ended questions to narrow**


**the scope of the issue, restate the issue, or question to verify**

- understanding).

**Use discretion and professionalism when discussing**

- experiences/encounters.
- Set and meet expectations/ timeline and communicate status with the customer.
- Offer repair/replacement options, as needed.
- Provide proper documentation on the services provided.
- Follow up with customer/user at a later date to verify satisfaction.

**Handling Customers’ Confidential and Private Materials**

- Located on a computer, desktop, printer, etc.

**Situation                   Correct Action**


**Customer password visible Keep confidential**


**Leaving PC unattended       Lock screen**


**Sensitive paper disposal    Shred documents**

- Accessing private files     Only when necessary

### 4.8 Explain the basics of scripting


**Common Script File Types**

  - .bat    — Batch File

**Explanation**

- Windows batch script executed by:
  - Command Prompt (cmd)
- Contains CMD commands.

**Common Uses**

  - automate tasks launch programs system administration
- Example

**@echo off**


**ipconfig**

- pause

**Scenario**

- Technician creates .bat file to clear temporary files automatically.

**Exam Memory Trick**


**.bat   = Windows Command Prompt script**

- .ps1   — PowerShell Script

**Explanation**

- Windows PowerShell script file.
- More powerful than batch files.

**Common Uses**


**administration**


**automation**


**Active Directory tasks**

- system management

**Example**

- Get-Process

**Scenario**

- Admin uses .ps1 script to create multiple user accounts automatically.

**Exam Memory Trick**


**.ps1   = PowerShell automation**

- .vbs   — VBScript

**Explanation**

- Visual Basic Script used mainly in older Windows automation.

**Common Uses**

  - legacy login scripts automation tasks

**Example**

- MsgBox "Hello"

**Scenario**

- Old company network still uses .vbs login scripts.

**Exam Memory Trick**


**.vbs   = older Windows scripting**

- .sh    — Shell Script

**Explanation**

- Linux/Unix shell script.

**Executed in:**

  - Bash shell terminal

**Common Uses**

  - Linux automation server tasks startup scripts

**Example**


**#!/bin/bash**

- ls

**Scenario**

- Linux admin creates .sh script for automatic backups.

**Exam Memory Trick**


**.sh   = Linux shell script**

- .js   — JavaScript File

**Explanation**

- JavaScript programming/script file.

**Mostly used in:**

  - web browsers web applications
  - Node.js
- Common Uses
  - webpage interactivity automation scripts

**Example**

- alert("Hello");

**Scenario**

- Website uses .js file for interactive login page.

**Exam Memory Trick**


**.js   = JavaScript/web scripting**

- .py   — Python Script

**Explanation**

- Python programming script.

**Popular for:**

  - automation scripting cybersecurity
  - AI/data work

**Example**

- print("Hello")

**Scenario**

- Technician uses Python script to monitor server logs automatically.

**Exam Memory Trick**

- .py   = Python script

**Use Cases for Scripting**

- Basic Automation

**Explanation**

- Scripts automate repetitive tasks automatically.

**Examples**

  - deleting temp files creating folders checking system status

**Scenario**

- Technician runs script every morning to clean temporary files.

**Exam Memory Trick**


**Automation = less manual work**

- Restarting Machines

**Explanation**

- Scripts can reboot/shutdown systems remotely or automatically.
- Common Uses

**after updates**


**frozen systems**

- scheduled maintenance

**Windows Example**

- Restart-Computer

**Linux Example**

- sudo reboot

**Scenario**

- Admin restarts 50 PCs remotely after patch deployment.

**Exam Memory Trick**


**Scripts help manage many devices quickly**

- Remapping Network Drives

**Explanation**

- Scripts automatically reconnect shared network drives.

**Windows Example**

- net use Z: \\Server\Shared

**Scenario**

- Employees log in and shared drive maps automatically.

**Exam Memory Trick**


**Map drive automatically at login**

- Installation of Applications

**Explanation**

- Scripts automate software installation.

**Common Uses**


**company-wide deployments**


**silent installs**

- standardized setups

**Scenario**

- IT deploys antivirus to all company PCs using script.

**Exam Memory Trick**


**Scripts = mass software deployment**

- Automated Backups

**Explanation**

- Scripts automatically copy/save important data.

**Common Uses**

- scheduled backups

**server backups**

- cloud synchronization

**Scenario**

- Nightly script backs up company files to backup server.

**Exam Memory Trick**


**Automated backups reduce data-loss risk**

- Gathering Information/Data

**Explanation**

- Scripts collect system information automatically.

**Examples**


**IP addresses**


**disk space**


**installed software**

- running processes

**Windows Example**

- Get-ComputerInfo

**Scenario**


**Technician gathers hardware info from all office PCs using PowerShell**

- script.

**Exam Memory Trick**

- Scripts collect data quickly
- Initiating Updates

**Explanation**

- Scripts trigger software/OS updates automatically.

**Common Uses**

  - Windows updates antivirus definitions
  - Linux package updates

**Scenario**

- Admin schedules script to update antivirus definitions daily.

**Exam Memory Trick**

- Scripts keep systems updated automatically

**Other Considerations When Using Scripts**

- Unintentionally Introducing Malware

**Explanation**

- Scripts can contain malicious code.

**Dangerous scripts may:**

  - install malware steal data create backdoors encrypt files

**Common Risk Sources**


**downloaded scripts from internet**


**email attachments**

- unknown GitHub repositories

**Scenario**

- User runs unknown PowerShell script downloaded from forum.
- Script installs ransomware silently.

**Prevention**


**use trusted sources**


**review script before running**


**use antivirus scanning**

- restrict script execution policies

**Exam Memory Trick**


**Unknown script = possible malware**

- Inadvertently Changing System Settings

**Explanation**


**Scripts can accidentally modify:**


**registry**


**permissions**


**network settings**

- services

**Risks**


**broken applications**


**login problems**

- network failures

**Scenario**

- Admin script accidentally disables Windows Firewall on all PCs.

**Prevention**


**test scripts first**


**use sandbox/lab**


**review commands carefully**

- create backups

**Exam Memory Trick**


**Scripts can change systems very quickly**

- Browser or System Crashes Due to Mishandling of Resources

**Explanation**


**Poorly written scripts may overuse:**


**CPU**


**RAM**


**storage**

- browser resources
- Possible Problems
  - freezing slow performance crashes infinite loops

**Scenario**

- Faulty JavaScript causes browser tab to freeze using 100% CPU.

**Another Scenario**

- Bad PowerShell loop consumes all RAM causing Windows instability.

**Prevention**

  - optimize scripts monitor resource usage test before deployment

**Exam Memory Trick**

- Bad scripts can overload systems

### 4.9 Remote Access Technologies


**Methods/tools**

- RDP (Remote Desktop Protocol)

**Explanation**

- Microsoft protocol for remote Windows desktop access.
- Default port:
- TCP 3389

**Common Uses**


**remote Windows administration**

- work-from-home access

**Scenario**


**Technician remotely controls employee Windows PC using Remote**

- Desktop.

**Security Considerations**


**use VPN + MFA**


**change default settings if possible**


**restrict internet exposure**

- brute-force attack risk

**Exam Memory Trick**


**RDP = Remote Windows desktop**

- VPN (Virtual Private Network)

**Explanation**

- Encrypted tunnel connecting remote users securely to network.

**Purpose**

- Protects traffic over internet.

**Scenario**

- Employee securely accesses company files from home through VPN.

**Security Considerations**


**use strong encryption**


**MFA recommended**

- stolen credentials risk

**Exam Memory Trick**


**VPN = secure encrypted connection**

- VNC (Virtual Network Computing)

**Explanation**

- Cross-platform remote desktop sharing technology.

**Can work on:**


**Windows**


**Linux**

- macOS

**Scenario**

- Technician remotely views Linux desktop using VNC.

**Security Considerations**


**weak/default passwords dangerous**

- encrypt traffic if possible

**Exam Memory Trick**


**VNC = cross-platform remote control**

- SSH (Secure Shell)

**Explanation**

- Encrypted command-line remote access.

**Mostly used for:**


**Linux**


**servers**

- networking devices
- Default port:
- TCP 22

**Scenario**

- Linux admin remotely manages Ubuntu server using SSH.

**Security Considerations**


**use key-based authentication**


**disable root login**

- brute-force attack risk

**Exam Memory Trick**


**SSH = secure Linux terminal access**

- RMM (Remote Monitoring and Management)

**Explanation**


**Centralized tool for:**


**monitoring devices**

- patch management remote support
- Used heavily by MSPs.
- (MSP = Managed Service Provider)

**Scenario**

- MSP remotely deploys antivirus updates to all client PCs.

**Security Considerations**


**compromise gives attacker large access**

- requires strong authentication/access control

**Exam Memory Trick**


**RMM = centralized IT management**

- SPICE (Simple Protocol for Independent Computing Environments)

**Explanation**

- Remote desktop protocol mainly used in virtual environments.

**Common in:**


**Linux virtualization**

- KVM/QEMU virtual machines

**Scenario**

- Admin remotely accesses Linux VM console using SPICE.

**Security Considerations**


**secure authentication needed**

- restrict unauthorized access

**Exam Memory Trick**


**SPICE = virtualization remote desktop**

- WinRM (Windows Remote Management)

**Explanation**

- Microsoft remote management protocol.
- Allows remote PowerShell/administration.

**Common Uses**


**remote scripting**


**automation**

- server management

**Scenario**

- Admin remotely runs PowerShell commands on multiple servers.

**Security Considerations**


**use HTTPS/Kerberos**

- restrict administrator access

**Exam Memory Trick**


**WinRM = remote PowerShell management**


**Third-Party Tools**

- Screen-Sharing Software

**Examples**

  - TeamViewer
- AnyDesk

**Purpose**

- Remote troubleshooting/support.

**Security Risks**


**unauthorized remote access**

- phishing/social engineering
- Videoconferencing Software

**Examples**


**Zoom**

- Microsoft Teams

**Security Risks**


**meeting hijacking**

- exposed meeting links
- File Transfer Software

**Purpose**

- Transfer files remotely.

**Examples:**


**FTP/SFTP tools**

- cloud sharing apps

**Security Risks**

- malware transfer
  - data leakage
  - Desktop Management Software
  - Purpose
  - Manage systems remotely at scale.
  - Examples:
  - patch deployment software inventory policy management

**Security considerations of each access method**


**Method             Major Risk**


**RDP                Internet exposure/brute force**


**VPN                Credential theft**


**VNC                Weak encryption/passwords**


**SSH                Key/password attacks**


**RMM                Large-scale compromise**


**WinRM              Remote admin abuse**


**Screen sharing     Scams/social engineering**


**Video meetings Unauthorized access**

- File transfer      Malware/data leaks

**Situation                             Best Practice**


**Remote access exposed to internet Use VPN**


**Remote login security                 MFA**


**Linux remote admin                    SSH**


**Secure file transfer                  SFTP**

- RDP security                          Restrict access + strong passwords

### 4.10 Basic concepts related to artificial intelligence

(AI).

**Application integration**


**Meaning:**

- AI is added into existing software/applications to automate or improve tasks.

> **Think:** 

**Email app with AI writing suggestions**


**Customer support chatbot**


**AI in spreadsheet analyzing data**

- AI inside ticketing/helpdesk software

> **Scenario:** 

**A company adds an AI chatbot into its website to answer customer**

- questions automatically.

> **Question:** 
- What AI concept is being used?

> **Answer:** 
- ✅ Application integration
- Because AI is integrated into an existing application.

**Policy**


#### 1. Appropriate Use

- Rules on what employees are allowed/not allowed to do with AI.

**Examples:**


**Can use AI for drafting emails**


**Cannot upload confidential customer files**

- Cannot ask AI to generate malicious scripts

> **Scenario:** 

**An employee pastes company financial data into a public AI tool without**

- permission.

> **Issue:** 
- ❌ Violates appropriate use policy

#### 2. Plagiarism

- Claiming AI-generated content as your own original work.

**Example:**


**Student submits AI-written essay as their own**

- Employee copies AI report without verification/citation

> **Scenario:** 
- A student uses AI to generate homework and submits it unchanged.

> **Answer:** 
- ✅ Plagiarism

**Limitations**


#### 1. Bias

- AI output is unfair because training data is unbalanced.

**Example:**


**Hiring AI prefers certain demographics because training data was**

- biased.

> **Scenario:** 

**An AI recruiting tool consistently rejects qualified candidates from one**

- group.

> **Answer:** 
- ✅ Bias

#### 2. Hallucinations

- AI generates false or made-up information confidently.
- Very testable.

**Example:**


**AI invents fake sources**

- AI gives wrong troubleshooting steps

> **Scenario:** 
- A chatbot gives a user a software command that does not exist.

> **Answer:** 
- ✅ Hallucination

> **Think:** 
- Hallucination = AI makes stuff up.

#### 3. Accuracy

- How correct/reliable AI output is.
- AI may give partially correct or outdated info.

> **Scenario:** 

**A technician verifies AI-generated troubleshooting steps before applying**

- them.

**Why?**

- ✅ To ensure accuracy

**Private vs. public**


#### 1. Private AI

- Internal/company-controlled AI.

**Examples:**


**Runs on company server**


**Only employees access it**

- Uses internal company data

**Benefits:**


**Better security**

- More control

> **Scenario:** 
- A hospital uses an internal AI system to analyze patient records securely.

> **Answer:** 
- ✅ Private AI

#### 2. Public AI

- Open to general public.

**Examples:**


**Public chatbot websites**

- Public image generators

> **Risk:** 
- Data exposure

> **Scenario:** 
- An employee uploads customer database to public AI website.

> **Risk:** 
- ❌ Public AI exposure