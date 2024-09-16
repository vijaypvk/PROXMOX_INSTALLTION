**OVERVIEW**:

Host machine config:
-  For primary storage, the host must have 2 x SSD/NVMe of same size to host all CT/VMs.
- Recommended to have 2 x HDD of same size for storing local backups.
-  All disks will have `zfs RAID1` to protect against disk failures. Eg. 2 x 1TB NVMe in zfs RAID1 set and 2 x 4TB SATA in another zfs RAID1 set.
- zfs is the preferred filesystem for local storage as it offer the [best storage features](https://pve.proxmox.com/pve-docs/chapter-pvesm.html) like snapshots, clone, replication, data protection, performance, etc.

## Installation Steps:

### Step 1: Start the Installer
![[Pasted image 20240821093211.png]]


### Step 2: Setup zfs RAID1 on NVMe/SSD disks:
![[Pasted image 20240821093255.png]]

Note:

1. Using zfs RAID1 is recommended to protect against disk failures.

See:

1. [ZFS on Linux](https://pve.proxmox.com/wiki/ZFS_on_Linux)
2. [Proxmox Storage Wiki](https://pve.proxmox.com/wiki/Storage)
3. [Proxmox Storage Manual](https://pve.proxmox.com/pve-docs/chapter-pvesm.html)
### Step 3: Time Zone Config

![[Pasted image 20240821093911.png]]

### Step 4: Administrator Password and Email Address
				
![[Pasted image 20240821094030.png]]


### Step 5: Management Network Configuration

![[Pasted image 20240821094523.png]]


### Step 6: Summary

![[Pasted image 20240821094628.png]]

## References

- Proxmox full course [https://www.youtube.com/playlist?list=PLT98CRl2KxKHnlbYhtABg6cF50bYa8Ulo](https://www.youtube.com/playlist?list=PLT98CRl2KxKHnlbYhtABg6cF50bYa8Ulo)
