# :computer: Network Deployment 
The Network Deployment project, completed in the ITE 253 Network Management II course, is a comprehensive network infrastructure implemented using a Dell PowerEdge R6515 Rack Server. The project spans from initial setup to configurations, including efficient IP management, DNS setup, enhancing network reliability with a secondary domain controller, and integrating Active Directory. This approach embodies a holistic strategy for creating a secure, scalable, efficient network environment.
- [:computer: Network Deployment](#computer-network-deployment)
  - [Initial Setup](#initial-setup)
    - [1. Fresh Install](#1-fresh-install)
      - [ Hardware Utilized ](#-hardware-utilized-)
      - [ Benefits and Drawbacks of Using Windows Server ](#-benefits-and-drawbacks-of-using-windows-server-)
      - [ Steps to Create a Bootable USB ](#-steps-to-create-a-bootable-usb-)
      - [ Driver Downloads ](#-driver-downloads-)
    - [2. Static Network Configuration](#2-static-network-configuration)
    - [3. DNS](#3-dns)
    - [4. Secondary Domain Controller](#4-secondary-domain-controller)
  - [DHCP](#dhcp)
    - [1. Enabling DHCP](#1-enabling-dhcp)
    - [2. Failover](#2-failover)
  - [Active Directory](#active-directory)
    - [1. Enabling Active Directory](#1-enabling-active-directory)

## Initial Setup

This section provides detailed guidelines for a fresh installation on a Dell PowerEdge R6515 Rack Server, highlighting hardware specifications, the benefits and drawbacks of using Windows Server, and a step-by-step guide to creating a bootable USB. We also include a link for downloading the necessary drivers.

### 1. Fresh Install

#### <u> Hardware Utilized </u>

**Model:** PowerEdge R6515 Rack Server

**Specifications:**
- **Processor:** AMD EPYC 7002 and 7003 series processors up to 64 cores
- **Memory:** Supports up to 2TB using 16 LRDIMM slots
- **Storage:** Flexible storage options with up to 10 x 2.5" SAS/SATA/SSD, NVMe SSD options available
- **Management:** Integrated Dell Remote Access Controller (iDRAC) with Lifecycle Controller for advanced management

This server is designed for data centers needing an efficient and secure platform to handle demanding workloads. It offers a balance of performance, capacity, and manageability.

#### <u> Benefits and Drawbacks of Using Windows Server </u>

**Benefits:**
- **Integrated Management Tools:** Windows Server provides powerful management tools such as Windows Admin Center and PowerShell, simplifying server administration.
- **Security:** Enhanced security features like Windows Defender Advanced Threat Protection and encrypted virtual machines help protect against modern security threats.
- **Hybrid Capabilities:** Seamless hybrid operations with Azure, including Azure Arc for managing Windows Server deployments across hybrid environments.

**Drawbacks:**
- **Cost:** Windows Server licensing can be expensive, especially for organizations with multiple servers.
- **Resource Intensity:** It may require more resources (CPU, RAM) compared to some lightweight Linux distributions, potentially impacting server efficiency.
- **Compatibility:** Certain applications, especially open-source ones, may have compatibility issues or may not be optimized for Windows Server environments.

#### <u> Steps to Create a Bootable USB </u>

1. **Download the ISO File:** Obtain the Windows Server 2022 ISO file from Microsoft. [Microsoft's Windows Server 2022 page](https://info.microsoft.com/ww-landing-windows-server-2022.html)
2. **Prepare USB Drive:** Ensure the USB drive has at least 8GB of storage and is formatted to FAT32 (detailed below).
3. **Use Rufus or a Similar Tool:** Download and run Rufus or another bootable USB creation tool. [Rufus .exe download](https://rufus.ie/en/)
4. **Configure Rufus:**
   - **Device:** Select your USB drive.
   - **Boot selection:** Click SELECT and browse to your downloaded ISO file.
   - **Partition scheme:** Choose GPT for UEFI firmware.
   - **File system:** Select FAT32.
   - **Volume label:** Name your drive as desired.
   - **Click START and wait for the process to complete.**

#### <u> Driver Downloads </u>

For optimal performance and compatibility, ensure you have the latest drivers for your PowerEdge R6515 Rack Server. You can find and download the necessary drivers from Dell's official support page: [PowerEdge R6515 Drivers Download](https://www.dell.com/support/home/en-us/product-support/product/poweredge-r6515/drivers).

Remember, a successful installation not only relies on following these steps carefully but also on understanding the specifics of your hardware and software environment. Always refer to the official documentation for the most accurate and up-to-date information.

### 2. Static Network Configuration
* Purpose of setting static configurations
* IP Address, Subnet Mask, Default Gateway, DNS
* Include pictures and directions
### 3. DNS
* Purpose of DNS
* Setting up DNS
* How to create zones, include pictures and directions
* Forward vs reverse lookup Zones

### 4. Secondary Domain Controller
* Purpose of Secondary Domain Controller
* How to set it up
* DNS (Include directions for STANDALONE DNS)
## DHCP
### 1. Enabling DHCP
* Purpose of DHCP
* Scopes
* Exclusions
### 2. Failover
* Purpose of Failover
* How to setup DHCP failover including pictures and directions

## Active Directory
### 1. Enabling Active Directory
* Purpose of Active Directory
* Group Policy Objects (GPOs)
* Organizational Units 