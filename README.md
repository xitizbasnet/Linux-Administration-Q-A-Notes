# 🐧 Linux Administration Q&A Notes

## 📘 Basics & Operating System

### ❓ Q1. What is Linux?
- 🆓 Linux is a **free and open-source** operating system kernel (the core part of the OS).
- 🧠 It works like a bridge between your computer’s **hardware** (CPU, memory, devices) and **software** (apps, programs), making sure resources are managed properly.

### 🔄 Q2. Difference between Linux and Unix?
- 🖥️ **Unix** is the original operating system made by companies, and each company has its own version (like IBM AIX, HP-UX, Solaris).
- 🐧 **Linux** is a free, open-source version that was created later, inspired by Unix. Instead of being owned by one company, it’s built and maintained by the **community**, and it comes in many flavors (like Ubuntu, CentOS, Debian, RedHat).
- 🌍 **Community**: A group of people around the world (developers, testers, and users) who work together to improve Linux.

### ⚙️ Q3. What are runlevels (or systemd targets)?
- 🔢 Runlevels are modes in Linux that decide which services and programs start when the system boots.
- 🧓 Older Linux used numbers 0–6 for runlevels:
  - `0` → 🔻 Shut down
  - `1` → 👤 Single-user mode (maintenance)
  - `3` → 🖥️ Multi-user text mode (no GUI)
  - `5` → 🖼️ Multi-user GUI (graphical desktop)
  - `6` → 🔁 Reboot
- 🆕 Modern Linux uses **systemd**, which replaced runlevels with **targets**.
- 📛 Targets are just like runlevels but easier to understand:
  - `poweroff.target` → `0` (🔻 Shutdown)
  - `rescue.target` → `1` (👤 Single-user)
  - `multi-user.target` → `3` (🖥️ Text mode)
  - `graphical.target` → `5` (🖼️ GUI)
  - `reboot.target` → `6` (🔁 Reboot)

### 🌟 Q4. Explain the basic features of Linux.
- 🆓 **Free and open-source**  
  _Example_: You can download Ubuntu without paying.
- 👥 **Multi-user support**  
  _Example_: On a server, 10 people can log in together.
- 🔄 **Multitasking**  
  _Example_: You can play music while browsing and copying files.
- 💻 **Cross-platform**  
  _Example_: Linux runs on laptops, servers, even Android phones.
- 🔐 **Secure and stable**  
  _Example_: Servers run for months without crashing.
- 🌐 **Strong networking features**  
  _Example_: You can easily set up a web or FTP server.
- 💪 **Powerful command line**  
  _Example_: A single command can copy 1000 files at once:  
  `cp *.txt /home/user/backup/`
- 🧑‍🤝‍🧑 **Large community support**  
  _Example_: If you face an error, you’ll find help on forums like AskUbuntu.

  ### Q5. Name some Linux Distributions
- **For general use:**
  - 🐧 Ubuntu – beginner-friendly, widely used
  - 🧪 Fedora – cutting-edge features
  - 🧱 Debian – very stable
  - 🧭 openSUSE – enterprise-friendly
  - 🌿 Linux Mint – good for Windows users
- **For servers:**
  - 🏢 CentOS Stream – stable for servers
  - 🛠️ RHEL – commercial support
  - 🌐 Ubuntu Server – popular for web servers
- **For special purposes:**
  - 🕵️ Kali Linux – ethical hacking
  - 🍓 Raspberry Pi OS – for Raspberry Pi
  - 🧩 Arch Linux – advanced users

  ## 🖥️ System Setup

### Q6. Difference between Linux and Windows
| Feature        | Linux                          | Windows                          |
|----------------|--------------------------------|----------------------------------|
| 💰 Cost         | Free                           | Paid (license required)          |
| 🔍 Source       | Open-source                    | Closed-source                    |
| 🔒 Security     | Very secure                    | More vulnerable                  |
| ⚡ Performance  | Lightweight                    | Needs more resources             |
| 🎨 Customization| Highly customizable            | Limited customization            |
| 💻 Software     | Lots of free software          | Most commercial software         |
| 🖥️ UI           | Varies by distro               | Consistent GUI                   |
| 🔄 Updates      | Frequent, user-controlled      | Automatic, sometimes forced      |
| 🧑‍💻 Use         | Servers, programming, tech users| Gaming, desktop, business        |

### 🧩 Q7. Components of Linux.
- Kernel – The core of Linux that talks to hardware (CPU, memory, devices).
- Shell – Command-line interface where users type commands.
- File System – Organizes files and directories on the system.
- System Libraries – Programs used by applications to interact with the kernel.
- System Utilities – Tools and programs for managing the system (copying files, managing users, etc.).
- Applications – Software you use, like browsers, editors, or games.
- 🧠 Simple way to remember: Kernel → Shell → Libraries → Utilities → Applications → Filesystem

### 🧠 Q8. What is the kernel? Is it legal to edit it?
- The kernel is the core part of Linux, like the brain of the system.
- It acts as a bridge between hardware and software, managing CPU, memory, devices, and processes.
- Example: When you open a web browser, the kernel decides how much CPU and memory it gets and how to talk to your network card.
- ✅ Yes, it is legal to edit the Linux kernel because Linux is open-source under the GPL license.
  - You can view, modify, and share it.
  - If you distribute your changes, you must also share them under the same license.
- 🧠 Easy way to remember: Kernel = brain of Linux, and you are allowed to tweak it legally!

### 💻 Q9. CLI vs GUI
- CLI (Command Line Interface)
  - You type commands to tell the computer what to do.
  - Fast and powerful, but harder for beginners.
  - Example: `ls` to list files, `cd` to change folder.
- GUI (Graphical User Interface)
  - You click icons and use menus to control the computer.
  - Easy to use, good for beginners, but slower than CLI.
  - Example: Using a browser, opening files by clicking.

### 🐚 Q10. What is Shell?
- A shell is a program that lets you communicate with Linux.
- You type commands, and the shell tells the kernel to do tasks.
- Acts as a bridge between the user and the system.
- Popular shells:
  - Bash (Bourne Again Shell) – Most popular, default in many Linux systems.
  - Sh (Bourne Shell) – Old, basic shell, used in scripts.
  - Ksh (Korn Shell) – Advanced features for scripting.
  - Csh (C Shell) – C-like syntax, good for programmers.
  - Tcsh – Improved version of Csh with auto-completion.
  - Zsh (Z Shell) – Powerful, customizable, with themes and plugins.

### 📂 Q11. What is a file system in Linux?
- A file system controls how data is stored and retrieved.
- Linux supports ext2, ext3, ext4, xfs, btrfs, etc.

### 🧾 Q12. What is inode?
- Inode is a data structure in Linux that stores file information (owner, permissions, timestamps, size, location), but not the filename.

### 🔗 Q13. Difference between hard link and soft link?
- Hard link: Points to the same inode (exact copy). File works even if original is deleted.
- Soft link: Shortcut that points to another file. If the original is deleted, the link breaks.

### 🧵 Q14. What is the difference between process and thread?
- Process is an independent program with its own memory.
- Thread is a lightweight sub-part of a process that shares memory.

### 🧩 Q15. What is init/systemd?
- init or systemd is the first process started by the kernel.
- It initializes system services, runs background daemons, and manages processes.

### 📁 Q16. Difference between absolute and relative path?
- Absolute path starts from the root `/` (e.g., `/home/user/file.txt`).
- Relative path is from the current directory (e.g., `./file.txt`).

### 💾 Q17. What is swap space?
- Swap is disk space used as virtual memory when physical RAM is full.
- Helps avoid crashes but is slower than RAM.

### 🧟 Q18. What is difference between process state Running and Zombie?
- Running: Process is active and using CPU.
- Zombie: Process finished execution but still exists in the process table waiting for parent cleanup.

### 🔍 Q19. What is difference between grep, find, locate?
- `grep`: Searches text patterns inside files.
- `find`: Searches files/directories by name, size, time, etc.
- `locate`: Quickly finds files using a pre-built database.

### 🧠 Q20. What is virtual memory?
- Virtual memory combines RAM and disk (swap).
- It allows running more programs than available physical RAM.

### 🔁 Q21. What is difference between booting and rebooting?
- Booting is starting the OS from scratch (power on).
- Rebooting is restarting the OS without power off.

### 🧾 Q22. How to check OS version?
- Use `cat /etc/os-release`.
- Shows name, version, and details of the distribution.


## 🛡️ Special Permissions

### 🧠 Q23. How to check kernel version?
- Run `uname -r`.
- Example: `5.10.0-25-amd64`

### Q24. What is SGID? 
- Files: group privileges; Directories: inherit group

### Q25. What is Sticky Bit? 
- Prevents deletion by others in shared dirs

### Q26. Set SUID, SGID, Sticky Bit?
- Can be set with chmod using octal or symbolic op ons.
- `chmod 4755 file.sh` # SUID
- `chmod 2775 dir` # SGID
- `chmod 1777 /tmp` # Sticky
 



 To proceed with formatting your content into a well-structured, GitHub-style Markdown document, you'll need to **log in to ChatGPT** to use the **ChatGPT canvas** feature. Once logged in, I can format everything for you in a `.md` file directly.

However, here’s a preview of how I’ll structure it:

---

# 🔐 Linux File Permissions & Security

## 📌 Special Permissions

### 1. ⚙️ SUID (Set User ID)

* Runs with the **owner’s privileges**, not the user’s.
* Useful for giving users **temporary elevated access**.

```bash
ls -l /usr/bin/passwd
```

**Output:**

```bash
-rwsr-xr-x 1 root root 54256 Oct  6 /usr/bin/passwd
# Notice the 's' in owner's execute field → SUID is set
```

**🧪 Test:**

* `/etc/shadow` is modifiable only by root.
* But `passwd` command has SUID → users can change their passwords safely.

---

### 2. 👥 SGID (Set Group ID)

* Runs with the **group’s privileges**.
* On directories: new files inherit **group ownership** (great for team collaboration).

```bash
mkdir /project
chgrp developers /project
chmod 2775 /project
ls -ld /project
```

**Output:**

```bash
drwxrwsr-x 2 root developers 4096 Oct 6 /project
# 's' in group’s execute field → SGID is set
```

**🧪 Test:**

* New files inside `/project` auto-inherit group `developers`.

---

### 3. 📌 Sticky Bit

* Applied to **directories**.
* Prevents users from deleting **others’ files**, even in world-writable dirs (like `/tmp`).

```bash
mkdir /shared
chmod 1777 /shared
ls -ld /shared
```

**Output:**

```bash
drwxrwxrwt 2 root root 4096 Oct 6 /shared
# 't' at the end → Sticky Bit is active
```

**🧪 Test:**

* User A creates `file1` in `/shared`.
* User B **cannot delete** it — only A or root can.

---

## 🔒 Password & Security

### 27. Where are passwords stored?

* In `/etc/shadow` (hashed, root-readable only).

```bash
grep bob /etc/shadow
```

### 28. How to lock/unlock user account?

```bash
sudo passwd -l bob  # lock
sudo passwd -u bob  # unlock
```

### 29. How to set password expiry?

```bash
sudo chage -M 90 bob
```

### 30. What is `/etc/sudoers`?

* Defines sudo permissions.
* Use `visudo` to edit safely:

```bash
sudo visudo
```

### 31. How to give sudo access to user?

```bash
sudo usermod -aG sudo bob
```

### 32. What does `rwxr-xr--` mean?

* Owner: full (`rwx`)
* Group: read + execute
* Others: read only

```bash
ls -l file.txt
```

### 33. Absolute vs Relative chmod?

```bash
chmod 755 file.txt  # Absolute
chmod u+x file.txt  # Relative
```

### 34. What if permission is `000`?

* No access at all (even owner).
* Only root can restore.

```bash
chmod 000 file.txt
```

### 35. `>` vs `>>`

```bash
echo "hello" > file.txt   # Overwrites
echo "world" >> file.txt  # Appends
```

### 36. Check effective permissions

```bash
ls -l file.txt
namei -l file.txt
```

### 37. ACL vs Normal Permissions

```bash
setfacl -m u:alice:rwx file.txt
```

### 38. Default permissions for new files/dirs

* Files = `666 - umask`
* Dirs = `777 - umask`

---

## 📁 Linux File System, Partition & Storage

### Q1. What is a file system?

* Organizes data on disk: structure, access, metadata.

**Examples:** `ext4`, `xfs`, `btrfs`

---

### Q2. What is an inode?

* Stores metadata (not file content).

```bash
ls -i file.txt
```

---

### Q3. What is a journaling file system?

* Logs changes before writing → prevents corruption.

**Examples:** `ext4`, `xfs`

---

### Q4. ext2 vs ext3 vs ext4

| Type | Journaling | Features                                  |
| ---- | ---------- | ----------------------------------------- |
| ext2 | ❌          | Basic                                     |
| ext3 | ✅          | Adds journaling                           |
| ext4 | ✅          | Faster, bigger files, backward compatible |

---

### Q5. Common file systems

| File System | Best For                    |
| ----------- | --------------------------- |
| ext4        | General purpose             |
| xfs         | High performance, big files |
| btrfs       | Snapshots, checksums        |

---

### Q6. How to check file system type?

```bash
df -T
```

---

### Q7. How to repair a file system?

```bash
fsck /dev/sdb1       # ext2/3/4
xfs_repair /dev/sdb1 # xfs
```

---

# 💽 Linux Storage, File System, Package Management & More

### Q8. What is a par on? 

* A  partition is a logical sec on of a disk that can have its own file system and can be managed separately.
* Example: /dev/sda1. 

```

## 📦 Partitions & Mounting

### 🔹 Q9. Types of Partitions

* Disks can have primary, extended, and logical par ons for organizing data.

* Primary → max 4 per disk, can contain OS or data 
* Extended → container for logical par ons 
* Logical → inside extended, can exceed 4 partitions

---

### 🔍 Q10. How to view partitions

* Commands to list and display partition details.

```bash
lsblk
fdisk -l
parted -l
```

---

### 🧱 Q11. How to create a partition

* Partition creation divides a disk into usable sections with a chosen file system.

```bash
fdisk /dev/sdb   # create
mkfs.ext4 /dev/sdb1
```

---

### 🧹 Q12. How to delete or modify a partition

```bash
fdisk /dev/sdb   # d → delete, w → write changes
```

---

### 📁 Q13. What is a mount point?

* A mount point is a directory where a partition or storage device is attached for access.

```bash
mount /dev/sdb1 /mnt/data
```

---

### 🏷️ Q14. Mounting using UUID or label

```bash
mount -U <UUID> /mnt/data
mount -L mydisk /mnt/data
```

---

### ⚙️ Q15. `/etc/fstab`

* Config file that defines partitions and options to auto-mount at boot.

```bash
/dev/sdb1 /mnt ext4 defaults 0 0
```

---

### 🧰 Q16. Mount options

| Option     | Description              |
| ---------- | ------------------------ |
| `ro`       | read-only                |
| `rw`       | read/write               |
| `noatime`  | skip access time updates |
| `defaults` | default options          |

---

## 📊 Disk Usage & Quotas

### 💾 Q17. Check disk usage

```bash
df -h          # overall usage
du -sh /dir    # specific directory
```

---

### 🗃️ Q18. Check free inodes

```bash
df -i
```

---

### 📏 Q19. Disk quota

```bash
edquota user1
```

---

## 🧱 LVM (Logical Volume Manager)

### 🧾 Q20. What is LVM?

* Flexible storage system combining disks into logical volumes.

---

### 🧩 Q21. LVM Terms

* **PV (Physical Volume)** → disk or partition
* **VG (Volume Group)** → group of PVs
* **LV (Logical Volume)** → usable volume from VG
* **Snapshot** → temporary copy for backup

---

### 🏗️ Q22. How to create LVM

```bash
pvcreate /dev/sdb1
vgcreate vg1 /dev/sdb1
lvcreate -L 10G -n data vg1
mkfs.ext4 /dev/vg1/data
```

---

### ➕ Q23. Extend LVM volume

```bash
lvextend -L +5G /dev/vg1/data
resize2fs /dev/vg1/data
```

---

### ➖ Q24. Reduce LVM volume

```bash
lvreduce -L 5G /dev/vg1/data
resize2fs /dev/vg1/data
```

---

### 📸 Q25. LVM snapshot

```bash
lvcreate -L 1G -s -n snap1 /dev/vg1/data
```

---

## 🔁 Swap Space

### 🔄 Q26. What is swap?

* Disk space used as virtual memory when RAM is full.

---

### 📈 Q27. Check swap usage

```bash
swapon -s
free -h
```

---

### ➕ Q28. Create or increase swap

```bash
fallocate -l 2G /swapfile
mkswap /swapfile
swapon /swapfile
```

---

## 🧬 RAID (Redundant Array of Independent Disks)

### 🔀 Q29. What is RAID?

| RAID Level | Description                   |
| ---------- | ----------------------------- |
| RAID 0     | Striping, fast, no redundancy |
| RAID 1     | Mirroring, safe               |
| RAID 5     | Striping + parity             |

---

### 🛠️ Q30. Configure RAID

```bash
mdadm --create /dev/md0 --level=1 --raid-devices=2 /dev/sdb /dev/sdc
```

---

### 📊 Q31. Monitor RAID

```bash
cat /proc/mdstat
mdadm --detail /dev/md0
```

---

### 🧩 Q32. Repair RAID

```bash
mdadm --add /dev/md0 /dev/sdd
```

---

## 📂 File & Directory Management

### 🧭 Q33. Absolute vs relative path

```bash
# Absolute
/home/user/file

# Relative
./file
```

---

### 🔗 Q34. Hard vs soft link

```bash
ln file1 file2     # Hard link
ln -s file1 link1  # Soft link
```

---

### 🔐 Q35. Check permissions & inode

```bash
ls -l
ls -i
```

---

### ⚙️ Q36. Change permissions & owner

```bash
chmod 755 file
chown user:group file
```

---

## 🧼 Checking & Repairing File Systems

### 🧪 Q37. Check filesystem

```bash
fsck /dev/sdb1         # ext2/ext3/ext4
xfs_repair /dev/sdb1   # xfs
```

---

### 📝 Q38. Filesystem info

```bash
df -T
```

---

# 📦 Linux Package Management

---

## 📁 1. What is a package in Linux?

* A compressed file containing software, config, and metadata.
* Examples: `vim`, `apache2`, `nginx`

---

## 📂 2. Types of Linux Packages

* **Debian-based** (.deb) → Ubuntu, Debian
* **Red Hat-based** (.rpm) → RHEL, CentOS

```bash
# Examples:
curl_7.68.0-1ubuntu2_amd64.deb
httpd-2.4.6-97.el7.centos.x86_64.rpm
```

---

## 🔍 3. DEB vs RPM

| Feature | DEB (Ubuntu/Debian) | RPM (RedHat/CentOS) |
| ------- | ------------------- | ------------------- |
| Format  | `.deb`              | `.rpm`              |
| Tools   | `dpkg`, `apt`       | `rpm`, `yum`, `dnf` |

---

## ⚙️ 4. What is a Package Manager?

* Installs, updates, removes, and resolves dependencies.

| Distro        | Package Manager     |
| ------------- | ------------------- |
| Ubuntu/Debian | `apt`, `dpkg`       |
| RHEL/CentOS   | `yum`, `dnf`, `rpm` |

---

## 🛠️ 5. Package Managers in Linux

* **Debian/Ubuntu:**

  * `dpkg` (low level)
  * `apt-get` / `apt` (high level)

* **RedHat/CentOS:**

  * `rpm` (low level)
  * `yum` / `dnf` (high level)

---

## 🔄 6. dpkg vs apt (Ubuntu/Debian)

```bash
sudo dpkg -i package.deb   # No dependency handling
sudo apt install nginx     # With dependencies
```

---

## 🔄 7. rpm vs yum/dnf (RHEL/CentOS)

```bash
sudo rpm -ivh file.rpm         # Manual
sudo yum install httpd         # Auto dependencies
```

---

## 📚 8. Basic Package Management Commands

### Debian/Ubuntu (apt/dpkg)

```bash
sudo apt install nginx
sudo apt remove nginx
sudo apt update
sudo apt upgrade
apt show nginx
sudo dpkg -i file.deb
```

### RHEL/CentOS (yum/dnf/rpm)

```bash
sudo yum install httpd
sudo yum remove httpd
sudo yum update
yum info httpd
sudo rpm -ivh file.rpm
```

---

## 📦 9. Check installed packages

```bash
# Ubuntu/Debian
dpkg -l | grep nginx

# RHEL/CentOS
rpm -qa | grep httpd
```

---

## 🔍 10. Find package for a file

```bash
dpkg -S /usr/bin/ls     # Debian
rpm -qf /usr/bin/ls     # RedHat
```

---

## 🌐 11. What is a Repository?

* Central server where packages are stored.

```bash
# Ubuntu repo location
/etc/apt/sources.list
```

---

## 💽 12. Local vs Remote Repository

* **Local** → USB/local server
* **Remote** → Internet mirror

---

## 🔗 13. What is dependency?

* Packages may need other libraries (dependencies).

```bash
# Example: nginx needs libc6, openssl, etc.
```

---

## 🧨 14. Dependency Hell

* Conflicts/missing dependencies.

✅ Solved by: `apt`, `yum`, `dnf`


---

## 🔐 15. What is GPG Key?

* Verifies authenticity & integrity of packages.

```bash
apt-key add key.gpg
```

---

## 🔄 16. update vs upgrade

```bash
sudo apt update     # Fetch latest list
sudo apt upgrade    # Install new versions
```

---

## 🧹 17. remove vs purge

```bash
sudo apt remove nginx   # Keeps config
sudo apt purge nginx    # Removes everything
```

---

## 🧽 18. clean vs autoclean vs autoremove

```bash
sudo apt clean           # Remove all cache
sudo apt autoclean       # Remove outdated cache
sudo apt autoremove      # Remove unused packages
```

---

## 🔁 19. yum vs dnf

| Tool | Version  | Notes                       |
| ---- | -------- | --------------------------- |
| yum  | RHEL 6/7 | Older                       |
| dnf  | RHEL 8+  | Faster, better dependencies |

```bash
dnf install nginx
```

---

## 🌐 20. Install without internet?

✅ Yes — via local repo or downloading `.deb` / `.rpm`

```bash
sudo dpkg -i package.deb
```

---

 

Here is your **Security & SELinux** content fully formatted in **GitHub-style Markdown** with icons, headings, and no changes to your original content — just properly structured, readable, and Markdown-friendly:

---

# 🛡️ Security & SELinux

---

## 🔐 Q1. What is SELinux?

* SELinux (Security Enhanced Linux) is a kernel module that enforces **mandatory access control (MAC)**.
* It restricts services and users more strictly than normal Linux permissions.
* Example: A web server cannot access `/etc/shadow` because SELinux blocks it.

---

## ❓ Q2. Why use SELinux?

* Protects files, programs, and users from unsafe actions.
* Limits access so programs only use what they need.
* Example: Apache can read `/var/www/html` but not system files.

---

## ⚙️ Q3. What are SELinux modes?

* `Enforcing`: Rules are applied and blocked if not allowed.
* `Permissive`: Rules are only logged, not blocked.
* `Disabled`: SELinux is turned off.

```bash
getenforce  # Shows mode: Enforcing, Permissive, or Disabled
```

---

## 📊 Q4. How to check SELinux status?

```bash
sestatus      # Shows if active and current mode
getenforce    # Shows current enforcement mode
```

---

## 📜 Q5. What is a policy?

* A set of rules defining what users and programs can do.
* Controls access to files, processes, and ports.
* Example: Targeted policy restricts only web server programs.

---

## 📂 Q6. Types of policies:

* **Targeted**: Only some programs restricted (default).
* **Strict**: All programs restricted (very secure).
* **MLS**: Multi-Level Security, used in high-security systems.
* Example: Most Ubuntu servers use **Targeted** policy.

---

## 🔍 Q7. How to check the current policy?

```bash
sestatus              # Shows policy type and mode
cat /etc/selinux/config  # Shows default policy
```

---

## 🏷️ Q8. What is a context?

* Label on files, processes, or ports.
* Shows who can use it, what type it is, and security level.
* Example: `system_u:object_r:httpd_sys_content_t:s0` for web files.

---

## 🔎 Q9. How to see file contexts?

```bash
ls -Z /var/www/html   # File contexts
ps -Z                 # Process contexts
```

---

## ✏️ Q10. How to change file context?

* **Temporary**:

```bash
chcon -t httpd_sys_content_t /var/www/html/index.html
```

* **Permanent**:

```bash
semanage fcontext -a -t httpd_sys_content_t "/var/www/html(/.*)?"
```

---

## 🧪 Q11. What are SELinux booleans?

* Settings that turn some rules on/off.
* Allows programs to do extra actions without changing policy.
* Example: `httpd_enable_homedirs` lets Apache access user home directories.

---

## 🧾 Q12. How to see booleans?

```bash
getsebool -a
```

* Example: `httpd_can_network_connect on` → web server can connect to network

---

## 🔁 Q13. How to change booleans?

* **Temporary**:

```bash
setsebool httpd_enable_homedirs on
```

* **Permanent**:

```bash
setsebool -P httpd_enable_homedirs on
```

---

## 🚨 Q15. How to find SELinux denials?

```bash
# Check logs
cat /var/log/audit/audit.log
ausearch -m avc -ts recent
sealert -a /var/log/audit/audit.log
```

* Example: Web server denied writing to `/var/www/html/uploads`

---

## 🧯 Q16. Temporarily disable enforcement

```bash
setenforce 0
```

* Example: Test a new program without blocking actions

---

## ⛔ Q17. Permanently disable SELinux

```bash
# Edit config
vi /etc/selinux/config
# Change:
SELINUX=disabled
```

* Reboot required

---

## 🛠️ Q18. How to fix permission problems?

```bash
restorecon -Rv /var/www/html
```

* Adjust booleans if needed

---

## 🌐 Q19. How does SELinux handle ports?

* Controls which programs can use network ports.
* Prevents unauthorized programs from using important ports.
* Example: Only Apache can use port 80 labeled `http_port_t`.

---

## ➕ Q20. How to add a custom port?

```bash
semanage port -a -t http_port_t -p tcp 8080
```

* Example: Allow Apache to run on port 8080

---

## 🌍 Q21. How does SELinux affect web servers?

* Controls which files or directories web servers can access.
* Stops unsafe scripts from running in wrong locations.
* Example: Apache cannot modify `/etc/passwd` because of SELinux.

---

## ⚙️ Q22. How to make services work?

* Set correct context:

```bash
chcon -R -t httpd_sys_content_t /var/www/html
```

* Adjust booleans:

```bash
setsebool -P httpd_enable_homedirs on
```

---

## 🧰 Q23. Important SELinux commands

| Command      | Description                     |
| ------------ | ------------------------------- |
| `getenforce` | Show current mode               |
| `sestatus`   | Show policy and mode            |
| `ls -Z`      | Show file context               |
| `chcon`      | Change context temporarily      |
| `semanage`   | Manage context, ports, booleans |
| `setsebool`  | Enable/disable booleans         |
| `restorecon` | Reset files to default context  |

* Example:

```bash
restorecon -Rv /var/www/html
```

---

## ✅ Q24. SELinux best practices

* Keep SELinux **enabled in enforcing mode**
* Use **booleans** or **fix contexts** instead of turning it off
* Example: Let Apache access only necessary directories instead of disabling SELinux

---


Got it! You want the **Firewall & Networking** info but with icons and a bit of formatting, like a clean cheat-sheet style. Here's a polished, easy-to-read version with icons and bullet points:

---

# 🔥 **Firewall & Networking Cheat Sheet**

---

### 1. 🌐 What is networking in Linux?

* Linux systems communicate using **IP addresses, ports, and protocols**
* Example: Host websites, share files

---

### 2. 🆔 What is an IP address?

* Unique ID for devices on a network
* IPv4 example: `192.168.1.10`
* IPv6 example: `fe80::1`
* Command:

  ```bash
  ip addr show
  ```

---

### 3. 🧩 What is a subnet mask?

* Divides IP into **network** and **host** parts
* Example: `255.255.255.0` (first 3 octets = network)

---

### 4. 🚪 What is a gateway?

* Device/IP connecting your network to outside (internet)
* Command:

  ```bash
  ip route
  ```
* Example gateway: `192.168.1.1`

---

### 5. 🔍 What is a DNS server?

* Converts domain names (google.com) into IP addresses
* Config file: `/etc/resolv.conf`

---

### 6. 🌍 Public vs Private IPs

* **Public IP**: reachable over internet
* **Private IP**: works only inside LAN (e.g., `192.168.x.x`)

---

### 7. 📋 List network interfaces

* Command:

  ```bash
  ip link show
  ```
* Or (older):

  ```bash
  ifconfig -a
  ```
* Example interface: `ens33`

---

### 8. 🛠️ Configure IP manually

```bash
ip addr add 192.168.1.10/24 dev ens33
ip link set ens33 up
```

---

### 9. 🏓 Check network connectivity

* Ping another system:

  ```bash
  ping 8.8.8.8
  ```
* Trace route path:

  ```bash
  traceroute google.com
  ```

---

### 10. 🛣️ What is routing?

* Decides path packets take
* Show routing table:

  ```bash
  ip route show
  ```

---

### 11. 🔄 Default route vs Static route

* **Default:** fallback route
* **Static:** manual route for specific networks
* Example:

  ```bash
  ip route add 10.0.0.0/24 via 192.168.1.1
  ```

---

### 12. 🔢 What is a port?

* Identifies specific services (e.g., HTTP=80, SSH=22)
* Show listening ports:

  ```bash
  netstat -tuln
  ```

---

### 13. 🔀 TCP vs UDP

* **TCP:** reliable, ordered (SSH, HTTP)
* **UDP:** faster, no guarantee (DNS, streaming)

---

### 14. 🔌 Common services & ports

| Service | Port | Protocol |
| ------- | ---- | -------- |
| HTTP    | 80   | TCP      |
| HTTPS   | 443  | TCP      |
| SSH     | 22   | TCP      |
| FTP     | 21   | TCP      |

---

### 15. 🛡️ What is a firewall?

* Controls traffic, blocks unauthorized access
* Example: Allow SSH only on port 22

---

### 16. 🧰 Common Linux firewalls

* **iptables:** old, manual
* **firewalld:** newer, zones, easier
* **ufw:** simplest, Ubuntu-friendly

---

### 17. ⚖️ iptables vs firewalld vs ufw

| Firewall  | Complexity | Features                   |
| --------- | ---------- | -------------------------- |
| iptables  | High       | Full control, manual rules |
| firewalld | Medium     | Dynamic, zones & services  |
| ufw       | Low        | Simple allow/deny commands |

---

### 18. 🔍 Check firewall status

* Firewalld:

  ```bash
  systemctl status firewalld
  ```
* UFW:

  ```bash
  ufw status
  ```
* iptables:

  ```bash
  iptables -L
  ```

---

### 19. ✅ How to open/allow a port

* firewalld:

  ```bash
  firewall-cmd --zone=public --add-port=80/tcp --permanent
  firewall-cmd --reload
  ```
* ufw:

  ```bash
  ufw allow 80/tcp
  ```
* iptables:

  ```bash
  iptables -A INPUT -p tcp --dport 80 -j ACCEPT
  ```

---

### 20. ❌ How to block a port

* firewalld:

  ```bash
  firewall-cmd --zone=public --remove-port=23/tcp --permanent
  firewall-cmd --reload
  ```
* ufw:

  ```bash
  ufw deny 23/tcp
  ```
* iptables:

  ```bash
  iptables -A INPUT -p tcp --dport 23 -j DROP
  ```

---

### 21. 🏷️ Allow/deny services by name

* firewalld:

  ```bash
  firewall-cmd --add-service=http
  ```
* ufw:

  ```bash
  ufw allow ssh
  ```

---

### 22. 🔢 Port-based vs Service-based rules

* **Port-based:** open/close port number
* **Service-based:** open/close named services

---

### 23. 📊 Check active connections

* netstat:

  ```bash
  netstat -tulnp
  ```
* ss (newer):

  ```bash
  ss -tulnp
  ```

---

### 24. 🔎 Check which process uses a port

```bash
lsof -i :22
```

---

### 25. 🛤️ Check routing table

```bash
ip route show
```

---

### 26. 🌐 Check DNS resolution

* `nslookup domain_name`
* `dig domain_name`

---

### 27. 🧭 Trace network path

```bash
traceroute google.com
```

---


# 🔥 Firewall & Networking (Continued)

---

### 28. ⚡ How to test bandwidth and speed?

* Start server:

  ```bash
  iperf3 -s
  ```
* Run client test:

  ```bash
  iperf3 -c server_ip
  ```
* Check internet speed:

  ```bash
  speedtest-cli
  ```

---

### 29. 🗂️ Common network config files

* `/etc/network/interfaces` → Debian/Ubuntu static config
* `/etc/sysconfig/network-scripts/ifcfg-eth0` → RHEL/CentOS config
* `/etc/resolv.conf` → DNS server addresses

---

### 30. 🔄 Static vs Dynamic IP

* Static IP: Manually assigned, never changes (good for servers)
* Dynamic IP: Assigned by DHCP, can change automatically

---

### 31. 🔒 What is VPN?

* Virtual Private Network encrypts internet traffic
* Secure connection to remote network over internet
* Examples: OpenVPN, WireGuard

---

### 32. 📜 How to check firewall logs?

* Firewalld:

  ```bash
  journalctl -u firewalld
  ```
* iptables:

  ```bash
  cat /var/log/messages | grep iptables
  ```
* UFW:

  ```bash
  cat /var/log/ufw.log
  ```

---

### 33. 🔁 NAT vs Port Forwarding

* NAT: Translates private IPs to public IPs
* Port Forwarding: Redirects traffic from a port to internal device

---

### 34. ✔️ Linux networking & firewall best practices

* Always enable firewall; allow only required ports/services
* Use strong passwords, secure protocols (e.g., SSH)
* Regularly monitor logs and network status

---

### 35. 📡 What is a protocol?

* Set of rules computers follow to communicate
* Defines data format, transmission, reception
* Examples:

  * TCP: reliable data transfer
  * HTTP: web pages

---

# ⚙️ Process & Scheduling

---

### 1. 🏃‍♂️ What is a process?

* Running program with unique **PID**
* Example: Opening Firefox creates a process with a PID

---

### 2. 👨‍👦 Parent and child process

* Parent creates child processes
* Child runs independently but originates from parent
* Example: `systemd` is parent starting other processes

---

### 3. 👻 What is a daemon?

* Background process without user interaction
* Starts on system boot
* Example: `sshd` for SSH connections

---

### 4. 🎭 Foreground vs Background process

* Foreground: runs in terminal, you wait
* Background: runs behind, terminal usable
* Example:

  ```bash
  ./script.sh &
  ```

---

### 5. 📝 Linux process states

* Running: using CPU
* Sleeping: waiting for event/input
* Stopped: paused by user
* Zombie: finished but still in system table
* View with:

  ```bash
  ps aux
  ```

---

### 6. 🧟 Zombie process

* Finished but still listed due to parent not collecting exit status
* Find with:

  ```bash
  ps -el | grep Z
  ```

---

### 7. 💤 Sleeping vs Stopped

* Sleeping: waiting automatically
* Stopped: paused manually, needs resume
* Pause:

  ```bash
  kill -STOP PID
  ```
* Resume:

  ```bash
  kill -CONT PID
  ```

---

### 8. 👀 View running processes

* Snapshot:

  ```bash
  ps
  ```
* Real-time:

  ```bash
  top
  ```
* Example:

  ```bash
  ps aux | grep firefox
  ```

---

### 9. 🚀 Start process in background

```bash
./myscript.sh &
```

---

### 10. 🔄 Bring background to foreground

```bash
fg %job_number
```

---

### 11. ❌ Kill a process

* Polite stop:

  ```bash
  kill PID
  ```
* Force stop:

  ```bash
  kill -9 PID
  ```

---

### 12. 🎚️ Change process priority (nice)

* Start with priority:

  ```bash
  nice -n 10 command
  ```
* Change running process:

  ```bash
  renice 5 -p PID
  ```

---

### 13. 📊 Check CPU & memory usage

* Real-time:

  ```bash
  top
  ```
* Sort by memory:

  ```bash
  ps aux --sort=-%mem
  ```

---

### 14. ⏲️ What is process scheduling?

* Kernel decides CPU time allocation
* Ensures fair process execution

---

### 15. 📜 Scheduling policies

| Policy      | Description                 | Example Use            |
| ----------- | --------------------------- | ---------------------- |
| SCHED_OTHER | Normal processes            | Firefox, apps          |
| SCHED_FIFO  | First-In-First-Out realtime | Audio tasks            |
| SCHED_RR    | Round-robin realtime        | Multiple video streams |

---

### 16. ⏳ What is a time slice?

* CPU time given to each process for execution
* Helps share CPU fairly

---

### 17. 🔄 Preemptive vs Non-preemptive

* Preemptive: Kernel can interrupt process anytime (Linux)
* Non-preemptive: Process runs until completion

---

### 18. 🔀 Context switching

* CPU switches between processes by saving/restoring states
* Enables multitasking

---

### 19. 📋 List jobs in terminal

```bash
jobs
```

---

### 20. ⏸️ Stop a running job

* Pause: `Ctrl+Z`
* Manual stop:

  ```bash
  kill -STOP PID
  ```

---

### 21. ▶️ Resume stopped job

* Foreground:

  ```bash
  fg %job_number
  ```
* Background:

  ```bash
  bg %job_number
  ```

---

### 22. 🆚 Job vs Process

* Job: Shell command started by user
* Process: Running program managed by kernel

---

### 23. ⏰ What is a cron job?

* Scheduled automatic task
* Configured via `crontab`
* Example:

  ```bash
  0 5 * * * /home/user/backup.sh
  ```

---

### 24. 🔄 Cron vs at jobs

* Cron: Repeats tasks periodically
* At: Runs once at scheduled time

---

### 25. 📅 List cron jobs

* User:

  ```bash
  crontab -l
  ```
* Root:

  ```bash
  sudo crontab -l
  ```

---

### 26. 🗑️ Remove cron jobs

* Delete all:

  ```bash
  crontab -r
  ```
* Edit specific jobs:

  ```bash
  crontab -e
  ```

---

### 27. ⚡ What is a signal?

* Message to process to control behavior
* Stop, continue, terminate, etc.

---

### 28. 🚦 Common signals

| Signal  | Meaning     |
| ------- | ----------- |
| SIGTERM | Polite stop |
| SIGKILL | Force stop  |
| SIGSTOP | Pause       |
| SIGCONT | Resume      |

---

### 29. ✉️ Send a signal

```bash
kill -SIGNAL PID
```

Example:

```bash
kill -SIGSTOP 1234
```

---

### 30. 🗓️ What is a scheduling policy?

* Decides CPU allocation per process for fairness and efficiency

---

 
---

# 🖥️ Linux Scheduling Policies

**Q31. Common Scheduling Policies:**

* **SCHED_OTHER (Default)**

  * 🔄 Normal programs.
  * ⏳ CPU time is shared fairly among all users.
  * 📌 Example: Apps like Firefox, LibreOffice.

* **SCHED_FIFO (First-In-First-Out)**

  * 🕐 Runs one process at a time in order of arrival.
  * 🔒 Process keeps CPU until done or waiting.
  * 🎧 Example: Real-time audio tasks.

* **SCHED_RR (Round-Robin)**

  * 🔄 Runs each process for a fixed time, then switches.
  * ⚖️ Fair for multiple real-time processes.
  * 📺 Example: Multiple video streams.

* **SCHED_BATCH**

  * 🗂️ For big background jobs.
  * 🚫 Doesn’t disturb normal apps.
  * 📊 Example: Data processing scripts.

* **SCHED_IDLE**

  * 💤 Runs only when CPU is free.
  * ⬇️ Lowest priority.
  * ⚙️ Example: Background system maintenance.

* **SCHED_DEADLINE**

  * ⏲️ Ensures process finishes within set time.
  * 🚨 For very time-sensitive tasks.
  * 🤖 Example: Robotics or multimedia apps.

---

**Q32. How to check a process’s scheduling policy?**

```bash
chrt -p <PID>
```

* 🔍 Shows policy and priority.
* Example: `chrt -p 1234` → outputs `SCHED_OTHER` or `SCHED_RR`.

---

**Q33. How to set scheduling policy for a process?**

* Set SCHED_FIFO with priority 10:

```bash
chrt -f -p 10 <PID>
```

* Set SCHED_RR with priority 20:

```bash
chrt -r -p 20 <PID>
```

* ⚡ Use real-time policy for critical tasks to run faster.

---

 

---

### ⚙️ Q34. Difference: Normal vs Real-time Scheduling

* 🟢 **Normal (SCHED_OTHER)**: Fair scheduling for regular apps.
* 🔴 **Real-time (SCHED_FIFO, SCHED_RR)**: High priority for critical tasks.
* 📌 *Example:* Video streaming needs real-time; Firefox uses normal.

---



# ⚙️ System Services

**Q1. What is systemd?**

* 🔧 systemd manages all services and processes on Linux.
* 🚀 Starts services at boot and keeps them running.
* 📌 Example: Starts `sshd` so you can log in remotely.

---

**Q2. What is a service in Linux?**

* 🛠️ A background program providing a function.
* 🔄 Runs automatically without user interaction.
* 🌐 Example: `nginx` runs a web server.

---

**Q3. Difference between service and process:**

* ⚙️ Process → any program running on Linux.
* 🔄 Service → long-running background program.
* Example: Firefox = process, `sshd` = service.

---

**Q4. How to check service status?**

```bash
systemctl status <service_name>
```

* 🔍 Shows if service is running, stopped, or failed.
* Example: `systemctl status sshd`

---

**Q5. How to start/stop a service?**

* ▶️ Start: `systemctl start <service_name>`
* ⏹️ Stop: `systemctl stop <service_name>`
* Example: `systemctl start apache2`

---

**Q6. How to enable/disable a service at boot?**

* 🔄 Enable: `systemctl enable <service_name>` (starts at boot)
* 🚫 Disable: `systemctl disable <service_name>` (doesn’t start at boot)
* Example: `systemctl enable sshd`

---

**Q7. How to restart or reload a service?**

* 🔄 Restart: `systemctl restart <service_name>` (stop + start)
* ♻️ Reload: `systemctl reload <service_name>` (reload config without stop)
* Example: `systemctl reload nginx`

---

**Q8. How to list all running services?**

```bash
systemctl list-units --type=service
```

* 📋 Lists all active services.

---

**Q9. Types of services:**

* 🟢 **simple** → service runs continuously
* 🔀 **forking** → service starts in background
* ⚡ **oneshot** → runs once then exits
* 🔔 **notify** → informs systemd when ready
* 💤 **idle** → runs only when CPU is free

---

**Q10. Examples of service types:**

* simple → `ssh.service`
* forking → `apache2.service`
* oneshot → `systemd-tmpfiles-setup.service`

---

**Q11. What is a unit?**

* 📄 Unit = file telling systemd how to manage something.
* Manages services, mounts, devices, timers, etc.
* Example: `ssh.service` (SSH), `home.mount` (mount home directory).

---

**Q12. Common unit types:**

* 🛠️ service → background programs (sshd, nginx)
* 🔌 socket → listens for network requests (cups.socket)
* 🎯 target → groups units for boot stages (multi-user.target)
* 📂 mount → mounts directories (home.mount)
* ⏰ timer → scheduled tasks (apt-daily.timer)

---

**Q13. How to view service logs?**

```bash
journalctl -u <service_name>
```

* 📜 Shows messages and errors from the service.
* Example: `journalctl -u sshd`

---

**Q14. How to view logs in real-time?**

```bash
journalctl -f
```

* 🕒 Shows live logs as they come in.

---

**Q15. What is a timer?**

* ⏰ Timer schedules automatic tasks like cron jobs.
* Can run once, repeatedly, or at specific times.
* Example: `apt-daily.timer` updates packages daily.

---

**Q16. How to check timers?**

```bash
systemctl list-timers
```

* 📅 Shows all scheduled timers and next run times.

---

**Q17. SysVinit vs Systemd:**

| Feature        | SysVinit                | systemd                |
| -------------- | ----------------------- | ---------------------- |
| Startup method | Sequential (one by one) | Parallel (faster boot) |
| Speed          | Slower                  | Faster                 |
| Management     | Harder                  | Easier                 |

---

**Q18. Best practices:**

* 🔒 Enable only needed services for security.
* 👀 Use `systemctl status` and logs to monitor.
* ⏲️ Prefer timers over cron for systemd integration.


---

### Servers

---

#### 1. YUM (Yellowdog Updater, Modified)

**Q1. What is YUM?**
📦 YUM is a tool used in RHEL, CentOS, and Fedora to install, update, and remove software easily.
🔧 It automatically resolves dependencies, so required packages are installed without manual effort.
💡 Example: `yum install vim` will install Vim along with any packages it needs to work.

**Q2. Difference between YUM and DNF**
⚡ DNF is the newer version of YUM used in latest RHEL/Fedora versions.
⚙️ It uses less memory, handles dependencies faster, and shows better error messages.
💡 Example: `dnf install vim` works like YUM but is faster.

**Q3. What is a repository?**
🗂️ A repository is a storage location (online or local) where software packages are kept.
🔍 Types include official (trusted by OS), third-party (from developers), and local/offline repositories.
💡 Example: CentOS base repo or EPEL repo.

**Q4. How to check installed packages?**
📋 `yum list installed` lists all installed packages with versions and repositories.
📊 Helps in tracking software already on the system.

**Q5. How to search for packages?**
🔎 `yum search package_name` allows finding software in repositories without installing it.
💡 Example: `yum search apache` lists all Apache-related packages.

**Q6. How to update all packages?**
⬆️ `yum update` downloads and installs the latest versions of all installed packages.
🛡️ Ensures system is secure and has latest features.

**Q7. Advantages of YUM**
✅ Automatically manages dependencies, keeps software updated, easy to use.
⚠️ Reduces chances of broken packages.

**Q8. How to check package info?**
ℹ️ `yum info package_name` displays version, repo source, size, and description.
💡 Example: `yum info vim` shows info about Vim package.

**Q9. How to clean cache in YUM?**
🧹 `yum clean all` removes downloaded package files to free up disk space.
✨ Keeps system tidy, especially after many installations or updates.

---

#### Samba

**Q1. What is Samba?**
🔗 Samba allows Linux systems to share files and printers with Windows systems.
🖥️ It uses the SMB/CIFS protocol to communicate with Windows machines.
💡 Example: A Linux folder can appear as a network drive in Windows.

**Q2. What protocol does Samba use?**
📡 SMB (Server Message Block) or CIFS (Common Internet File System).
🔒 Handles authentication, file access, and printing services over a network.

**Q3. Difference between SMB and NFS**
🌐 SMB → cross-platform, works with Windows and Linux, good for mixed networks.
⚡ NFS → mainly for Linux/Unix networks, faster for Linux-only systems.

**Q4. Advantages of Samba**
👍 Easy file sharing between Linux and Windows, supports user authentication, permissions, and encrypted passwords.

**Q5. How to check connected users?**
👥 `smbstatus` shows active users, open files, and shared folders.
📈 Helps in monitoring network usage.

**Q6. How to monitor shared folder access?**
📂 Samba logs in `/var/log/samba/` record file access, login attempts, and errors.

**Q7. Security features of Samba**
🔐 Supports user-level authentication, share-level security, password encryption.
🛡️ Allows setting permissions for read/write access per user or group.

**Q8. What is a Samba domain controller?**
🖥️ Linux can act as a central authentication server for Windows clients.
🔑 Users log in with one account for network resources.

**Q9. Difference between Workgroup and Domain in Samba**
👥 Workgroup → peer-to-peer, each system manages its own users.
🏢 Domain → centralized user management, better for larger networks.

---

#### Apache

**Q1. What is Apache?**
🌐 Apache is a web server that hosts websites on Linux.
📡 It listens on HTTP/HTTPS ports and serves web pages to clients.
💡 Example: Hosting `http://example.com` on a Linux server.

**Q2. Advantages of Apache**
🛠️ Open-source, flexible, supports modules for additional features.
🔒 Works on almost all platforms and supports secure connections with SSL/TLS.

**Q3. Common ports used**
🔌 HTTP → 80, HTTPS → 443.
🌐 Ports allow web browsers to connect to the server.

**Q4. Difference between Apache and Nginx**
⚙️ Apache → process/thread-based, good for dynamic content, highly configurable.
🚀 Nginx → event-driven, handles high traffic better, faster for static content.

**Q5. How to check running websites?**
📋 `systemctl status httpd` or `netstat -tuln` to see active web services.

**Q6. How to monitor logs?**
📂 `/var/log/httpd/access_log` → tracks page visits.
📂 `/var/log/httpd/error_log` → shows errors and failures.

**Q7. What is a virtual host?**
🌍 Allows hosting multiple websites on one server using different domains or ports.
💡 Example: `example.com` and `test.com` on same IP.

**Q8. Advantages of SSL/TLS**
🔒 Encrypts data between client and server to protect sensitive information.

**Q9. What is mod_rewrite?**
🔄 Apache module to rewrite URLs for SEO, redirection, or user-friendly URLs.

**Q10. Difference between static and dynamic content**
🖼️ Static → fixed files like HTML, images.
⚙️ Dynamic → generated using scripts like PHP or Python.


---

# 🌐 DNS (Domain Name System)

**Q1. What is DNS?**

* 🔄 Translates human-friendly domain names into IP addresses.
* 🌍 Makes browsing easier without memorizing IPs.
* 📌 Example: `google.com` → `172.217.0.46`

**Q2. Common DNS record types:**

* 🅰️ A → IP address
* 🔗 CNAME → Alias
* 📧 MX → Mail server
* 🖥️ NS → Name server

**Q3. Authoritative vs Recursive DNS:**

* 📖 Authoritative: Final answer source for a domain.
* 🔍 Recursive: Queries other DNS servers to find answers.

**Q4. DNS Ports:**

* 🛡️ UDP 53 → DNS queries
* 🔄 TCP 53 → Zone transfers

**Q5. Advantages of DNS:**

* 🌐 Human-friendly URLs
* ⚡ Faster with caching
* 🚫 No need to remember IPs

**Q6. DNS Caching:**

* 💾 Temporarily stores IPs locally to speed lookups.

**Q7. Forward vs Reverse DNS:**

* 🔄 Forward: Domain → IP
* ↩️ Reverse: IP → Domain

**Q8. Troubleshooting Commands:**

```bash
dig example.com        # Detailed DNS info  
nslookup example.com   # Quick resolution check
```

**Q9. What is a zone file?**

* 📄 Text file on DNS server storing domain records (IPs, aliases, mail servers).

---

# 📡 DHCP (Dynamic Host Configuration Protocol)

**Q1. What is DHCP?**

* 🚦 Automatically assigns IP addresses and network settings.
* ⏱️ Saves manual configuration time.
* 📌 Example: Laptop gets IP `192.168.1.10` automatically.

**Q2. How DHCP works (DORA process):**

* 🔎 Discover → 📢 Offer → ✔️ Request → ✅ Acknowledge

**Q3. Static vs Dynamic IP:**

* 🛑 Static: Manually set, permanent.
* 🔄 Dynamic: Assigned automatically, can change.

**Q4. DHCP Lease Time:**

* ⏳ Duration device can use assigned IP.
* 🔄 Lease expiry may assign a new IP.

**Q5. DHCP Options:**

* ⚙️ Extra info like gateway, DNS, subnet mask.
* Example: Option 3 = Gateway, Option 6 = DNS.

**Q6. DHCP vs Manual IP:**

* 🔄 DHCP: Automatic, fewer errors.
* ⚙️ Manual: Full control, but more setup.

**Q7. Check DHCP assigned IPs:**

```bash
dhclient -v  
cat /var/lib/dhcp/dhclient.leases
```

**Q8. Security considerations:**

* 🚨 Rogue DHCP servers can disrupt networks.
* 🔐 Use network controls to authorize DHCP servers.

**Q9. DHCP Ports:**

* 🖥️ UDP 67 → Server
* 💻 UDP 68 → Client

**Q10. Troubleshooting DHCP:**

* 🔌 Check cables and switch ports
* ✅ `systemctl status dhcpd`
* 🔄 Release old IP: `dhclient -r` and request new IP: `dhclient`

---

# 📊 Monitoring & Performance

**Q1. What is system monitoring?**

* 📈 Checks CPU, memory, disk, network health.
* ⚠️ Detects problems before failure.

**Q2. Check CPU usage:**

```bash
top        # Real-time CPU, memory, processes  
mpstat     # Per-core CPU usage
```

**Q3. Check memory usage:**

```bash
free -h    # Total, used, free memory  
vmstat     # Memory and system stats
```

**Q4. Check disk usage:**

```bash
df -h      # Disk space by partition  
du -sh /path  # Size of folder
```

**Q5. Monitor running processes:**

```bash
ps aux  
top or htop
```

**Q6. Check network usage:**

```bash
ifconfig or ip -s link  
netstat -tulnp
```

**Q7. Advanced monitoring tools:**

* 📊 `sar` → Historical stats
* 📉 `iotop` → Real-time disk I/O
* 📈 `nload` → Visual network traffic

**Q8. Identify bottlenecks:**

* 🔥 High CPU → top, mpstat
* 🧠 Low memory → free -h, vmstat
* 💽 Disk I/O → iostat, iotop

**Q9. Improve CPU performance:**

* 🛑 Stop unneeded processes
* ⚡ Use `nice` to prioritize

```bash
nice -n -5 ./script.sh
```

**Q10. Improve memory usage:**

* ❌ Close unused apps
* 💾 Use swap if low memory

```bash
swapon -s
```

**Q11. Improve disk performance:**

* 🚀 Use SSDs
* 🗑️ Remove unnecessary files
* 🔍 Check heavy I/O with iotop

**Q12. Monitor service performance:**

```bash
systemctl status <service_name>  
journalctl -u <service_name>
```

---

# 🔐 SSH (Secure Shell)

**Q13. What is SSH?**

* 🔒 Secure remote access to Linux systems.
* 🔑 Encrypts communication.
* 📌 Example: `ssh user@192.168.1.10`

**Q14. Check SSH status:**

```bash
systemctl status sshd
```

**Q15. Connect to server:**

```bash
ssh user@server_ip
```

**Q16. Change SSH port:**

* ✍️ Edit `/etc/ssh/sshd_config` → change `Port 22`
* 🔄 Restart SSH: `systemctl restart sshd`

**Q17. Use SSH keys:**

* 🔑 Generate keys: `ssh-keygen`
* 📤 Copy public key: `ssh-copy-id user@server_ip`

**Q18. Secure SSH:**

* 🚫 Disable root login: `PermitRootLogin no`
* 🔐 Use key-based authentication
* 🔄 Change default port

**Q19. Check SSH logs:**

* Debian/Ubuntu: `/var/log/auth.log`
* RHEL/CentOS: `/var/log/secure`

**Q20. What is an SSH key?**

* 🔑 Key pair (public + private) for password-less login.

**Q21. Generate SSH keys:**

```bash
ssh-keygen -t rsa -b 4096
```

**Q22. Copy SSH key to server:**

```bash
ssh-copy-id user@server_ip
```

**Q23. Secure SSH keys:**

* 🔒 Use strong passphrases
* 🚫 Disable password login (`PasswordAuthentication no`)

---

# 🔗 Links (Hard vs Soft)

**Q24. What is a hard link?**

* 🔗 Another name for the same file (same inode).
* 🔄 Changes in one affect the other.

**Q25. Hard link characteristics:**

* ❌ Cannot link directories
* ❌ Cannot cross file systems
* 🗑️ Deleting one doesn’t remove data until all are deleted.

**Q26. Check hard links:**

```bash
ls -l   # Shows number of links  
ls -i file1 file2  # Same inode means hard link
```

**Q27. What is a soft link (symbolic link)?**

* 🔗 Shortcut to another file (different inode).
* 🛤️ Points to file path, can cross file systems.

**Q28. Soft link characteristics:**

* ✅ Can link directories
* ✅ Can cross file systems
* ⚠️ Broken if original deleted.

**Q29. Check soft links:**

```bash
ls -l    # Shows link1 -> file1  
file link1  # Identifies symbolic link
```

---

**Key differences:**

| Feature                  | Hard Link    | Soft Link (Symbolic Link) |
| ------------------------ | ------------ | ------------------------- |
| Inode                    | Same inode   | Different inode           |
| Directories              | Cannot link  | Can link                  |
| Cross Filesystems        | Cannot cross | Can cross                 |
| Broken if target deleted | No           | Yes                       |

---

 
