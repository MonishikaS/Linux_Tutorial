
# ⭐ **DAY 3 — Linux File System Structure (FHS) for System Administrators**

Linux organizes everything into a **tree-like structure** starting from the root directory `/`.

This structure is defined by **FHS (Filesystem Hierarchy Standard)**.

A good admin must know **what each directory contains** and **when to use it**.

---

# 🌳 **Root Directory: /**

“/” is the root of the entire filesystem. Everything (files, devices, applications) starts from here.

---

# 📁 **1. /bin — Essential User Commands**

Contains basic commands available to all users.

Examples:

```
ls   cd   cp   mv   rm   cat   mkdir
```

➡ Used in single-user or rescue mode
➡ Required for system boot

---

# 📁 **2. /sbin — System Admin Commands**

Contains commands mainly for **system administration**.

Examples:

```
reboot   shutdown   fdisk   ifconfig   ip   mount
```

➡ Only root should run them
➡ Used to configure system settings

---

# 📁 **3. /etc — Configuration Files**

One of the MOST important directories.

Contains ALL system configuration files.

Examples:

```
/etc/passwd       → user accounts
/etc/shadow       → encrypted passwords
/etc/hosts        → local hostname mappings
/etc/fstab        → disk mount info
/etc/ssh/sshd_config → SSH server config
```

➡ When you tune, configure, secure, or automate Linux → you edit `/etc` files.

Never delete files here.

---

# 📁 **4. /home — User Home Directories**

Stores personal files for regular users.

Examples:

```
/home/monishika
/home/john
```

Each user gets a folder with:
Downloads, Documents, Bash history, SSH keys, etc.

Root’s home is SPECIAL and located in **/root**, not inside /home.

---

# 📁 **5. /root — Root User’s Home Directory**

The **superuser’s home directory**.

* Used for admin scripts
* Secure access
* Only root has permission

Do not confuse `/root` with `/`.

---

# 📁 **6. /var — Variable Files**

Contains files that **grow over time**.

Important subfolders:

```
/var/log       → system logs
/var/mail      → emails
/var/spool     → jobs waiting to be processed
/var/www       → web server data
/var/tmp       → temporary files
```

As an admin:

* Check `/var/log/messages`, `/var/log/secure` for troubleshooting
* Always monitor `/var` usage to avoid disk full issues

---

# 📁 **7. /usr — User-related Programs (NOT home folder!)**

Contains installed software and libraries.

Subdirectories:

```
/usr/bin     → application commands
/usr/sbin    → admin commands
/usr/lib     → libraries
/usr/share   → documentation, icons
```

Many think `/usr` means “user home” — but it means **Unix System Resources**.

---

# 📁 **8. /opt — Optional Software**

Used for installing **third-party applications** manually.

Example:

```
/opt/apache
/opt/tomcat
/opt/myproject
```

As admin:

* Install custom apps here (not in /usr/bin)
* Clean, organized, easy to maintain

---

# 📁 **9. /tmp — Temporary Files**

Used by users and applications for temporary storage.

* Auto-cleaned on reboot
* Not secure
* Anyone can write here

For security, don’t store confidential files.

---

# 📁 **🔟 /dev — Device Files (Very Important)**

Linux treats devices as files.

Examples:

```
/dev/sda    → hard disk
/dev/sr0    → CD/DVD
/dev/tty    → terminals
/dev/null   → black hole device
```

Admin tools like `mount`, `fdisk`, `lsblk` interact with `/dev`.

---

# 📁 **1️⃣1️⃣ /proc — Virtual Kernel Filesystem**

Contains **kernel and process information**.

Examples:

```
/proc/cpuinfo
/proc/meminfo
/proc/uptime
/proc/1   → init/systemd process
```

Everything here is **virtual**, created by the kernel on the fly.

---

# 📁 **1️⃣2️⃣ /sys — Kernel + Hardware Info**

Created by the kernel for device management.

Used by drivers and low-level admin tools.

---

# 📁 **1️⃣3️⃣ /boot — Boot Loader Files**

Contains files needed to boot Linux.

Examples:

```
vmlinuz       → Linux kernel
initramfs     → initial RAM filesystem
grub2         → boot loader configuration
```

⚠ Changing files here can break your system.

---

# 📁 **1️⃣4️⃣ /lib and /lib64 — System Libraries**

Stores essential shared libraries needed for programs to run.

Equivalent to Windows **DLLs**.

---

# 📁 **1️⃣5️⃣ /run — Runtime Data**

Stores volatile runtime data created after boot.

Example:

```
/run/systemd
/run/user/1000
```

Cleared at reboot.

---

# ⭐ **DAY 3 Summary (You MUST Remember This Table)**

| Directory | Purpose                        |
| --------- | ------------------------------ |
| /bin      | User commands                  |
| /sbin     | Admin commands                 |
| /etc      | Configuration files            |
| /home     | User home directories          |
| /root     | Root user home                 |
| /var      | Logs, spool, dynamic data      |
| /usr      | Installed programs & libraries |
| /opt      | Third-party software           |
| /tmp      | Temporary files                |
| /dev      | Device files                   |
| /proc     | Kernel and process info        |
| /sys      | Kernel hardware interface      |
| /boot     | Boot loader files              |
| /lib      | Shared libraries               |

---

# 🧪 **Day 3 Practice Tasks (Do These on RHEL VM)**

1️⃣ List all directories in root:

```
ls /
```

2️⃣ Check who uses most disk in /var:

```
du -sh /var/*
```

3️⃣ View your system logs:

```
less /var/log/messages
less /var/log/secure
```

4️⃣ View kernel info:

```
cat /proc/cpuinfo
cat /proc/meminfo
```

5️⃣ Check bootloader files:

```
ls /boot
```

6️⃣ Create a folder under /opt and place a file:

```
sudo mkdir /opt/myapp
sudo touch /opt/myapp/readme.txt
```
---
