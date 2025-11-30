
# **📘 30-Day RHEL Learning Roadmap (Beginner → Admin)**

*(1 hour/day is enough — more time = faster progress)*

---

## **WEEK 1 — Linux & RHEL Foundations**

### **⭐ Day 1: Introduction to RHEL**

* What is Linux & RHEL?
* Editions, subscriptions, repos
* Install RHEL on VM (VirtualBox / VMware)

### **⭐ Day 2: Basic Linux Commands**

* pwd, cd, ls, cat, cp, mv, rm
* mkdir, touch, man
* File types, absolute vs relative path

### **⭐ Day 3: File System Structure**

* /root, /etc, /bin, /sbin, /home
* /var, /usr, /opt
* Understanding FHS (Filesystem Hierarchy Standard)

### **⭐ Day 4: File Permissions**

* chmod, chown, chgrp
* rwx permissions
* symbolic & numeric (777/755) modes

### **⭐ Day 5: Users & Groups**

* useradd, passwd, usermod, userdel
* groupadd, gpasswd
* /etc/passwd, /etc/shadow, /etc/group

### **⭐ Day 6: Text Editing with vi/vim**

* Insert, command, visual mode
* Editing, saving, searching
* Practice in /etc configs

### **⭐ Day 7: Package Management**

* yum, dnf commands
* enable/disable repos
* rpm commands

---

## **WEEK 2 — System Administration Basics**

### **⭐ Day 8: System Services**

* systemctl start/stop/status
* enable/disable services
* service logs (journalctl)

### **⭐ Day 9: Process & Job Management**

* ps, top, htop
* kill, nice, renice
* jobs, fg, bg

### **⭐ Day 10: Storage Management**

* fdisk, gdisk
* mkfs, mount, umount
* /etc/fstab

### **⭐ Day 11: LVM (Logical Volume Manager)**

* pvcreate, vgcreate, lvcreate
* Extend & reduce volumes
* lvs, vgs, pvs

### **⭐ Day 12: File System Permissions (Advanced)**

* ACLs (getfacl / setfacl)
* umask
* SUID, SGID, sticky bit

### **⭐ Day 13: Networking Basics**

* ip addr, nmcli
* /etc/hosts
* hostnamectl
* ping, curl

### **⭐ Day 14: Firewalld Basics**

* firewall-cmd
* Open/close ports
* Zones

---

## **WEEK 3 — Intermediate System Admin**

### **⭐ Day 15: SELinux Introduction**

* Modes: enforcing/permissive/disabled
* semanage, restorecon
* View logs

### **⭐ Day 16: Cron Jobs**

* crontab syntax
* system-wide vs user cron
* Automate tasks

### **⭐ Day 17: System Logs & Monitoring**

* /var/log
* journalctl advanced commands
* log rotation

### **⭐ Day 18: Storage Management (Advanced)**

* RAID basics
* Auto-mounting
* Troubleshooting disks

### **⭐ Day 19: Shell Scripting Basics**

* Variables, loops, conditions
* Write simple scripts
* Run scripts via cron

### **⭐ Day 20: Boot Process**

* GRUB2
* systemd targets
* rescue & emergency mode

### **⭐ Day 21: Backup & Restore**

* tar, rsync
* Backup strategies
* Optional: create backup scripts

---

## **WEEK 4 — Server Administration (RHEL Real-World Skills)**

### **⭐ Day 22: Apache Web Server**

* Install httpd
* Configure virtual hosts
* Manage firewall for port 80/443

### **⭐ Day 23: FTP / SFTP Server**

* vsftpd basics
* User restrictions
* Test with FileZilla

### **⭐ Day 24: Samba File Server**

* Install & configure Samba
* Share & access directories
* Permissions

### **⭐ Day 25: NFS Server**

* Export directories
* Mount from client
* Permissions & security

### **⭐ Day 26: SSH Configuration**

* Password vs key-based login
* sshd_config settings
* Fail2ban (optional)

### **⭐ Day 27: KVM Virtualization (Optional but useful)**

* Install & configure KVM
* virt-manager & virsh basics

### **⭐ Day 28: Git & Basic DevOps Tools**

* git init, clone, push
* yum install ansible
* First Ansible playbook

---

## **WEEK 5 — Final Admin Skills + Practice**

### **⭐ Day 29: Troubleshooting Day**

* Network issues
* Boot issues
* Permission problems
* Log-based debugging

### **⭐ Day 30: RHEL Practice Projects**

Pick any 2 mini projects:

* Setup a web server with firewall + SELinux
* Create new LVM volumes & mount
* Create 5 users with specific permissions
* Setup SSH key login
* Schedule daily backup via cron

---
