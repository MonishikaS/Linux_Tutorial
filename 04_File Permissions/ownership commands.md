# ⭐ **DAY 4 — Linux File Permissions, Ownership & ACLs (Admin Level)**

Linux permissions control **who can read, write, or execute** files and directories.

Every file has 3 layers of ownership:

1. **User (Owner)**
2. **Group**
3. **Others**

Each layer has 3 permission types:

* **r = read**
* **w = write**
* **x = execute**

---

# 🔹 **1. Understanding Permission Format (ls -l)**

Run:

```
ls -l
```

Example output:

```
-rwxr-xr-- 1 root admin 2048 Jan 10 script.sh
```

Breakdown:

```
-     rwx     r-x     r--
type  user    group   others
```

### Meaning:

* **User:** rwx → owner can read, write, execute
* **Group:** r-x → group can read + execute
* **Others:** r-- → others can only read

---

# 🔹 **2. File Types (First Character)**

| Symbol | Meaning              |
| ------ | -------------------- |
| -      | Regular file         |
| d      | Directory            |
| l      | Symbolic link        |
| b      | Block device (disks) |
| c      | Character device     |
| s      | Socket               |
| p      | Pipe                 |

Example:

```
drwxr-xr-x  → directory
-rw-r--r--  → normal file
```

---

# 🔹 **3. Changing File Permissions (chmod)**

### **Symbolic Method**

```
chmod u+r file        → give read to user
chmod g-w file        → remove write from group
chmod o+x file        → give execute to others
chmod a+r file        → give read to all (ugo)
```

### **Numeric Method**

| Permission | Value |
| ---------- | ----- |
| r          | 4     |
| w          | 2     |
| x          | 1     |

Examples:

```
chmod 755 file     → rwx r-x r-x
chmod 644 file     → rw- r-- r--
chmod 700 file     → rwx --- ---
chmod 600 file     → rw- --- ---
```

---

# 🔹 **4. Changing Ownership (chown)**

### Change owner:

```
chown user file
```

### Change owner + group:

```
chown user:group file
```

### Example:

```
chown root:root /opt/app
```

---

# 🔹 **5. Changing Group Ownership (chgrp)**

```
chgrp developers project.txt
```

---

# 🔹 **6. Directory Permissions**

Permissions work differently for directories:

| Permission | Effect              |
| ---------- | ------------------- |
| r          | list files          |
| w          | create/delete files |
| x          | enter directory     |

Example:

```
chmod 755 folder
```

Means:

* Owner: full access
* Group: browse + list
* Others: browse + list

---

# 🔹 **7. Special Permissions (SUID, SGID, Sticky Bit)**

### **SUID (Set User ID)**

File runs with **owner's privilege**.

Example:

```
chmod 4755 file
```

Used for commands like:

```
/usr/bin/passwd
```

(Always runs as root)

---

### **SGID (Set Group ID)**

New files inherit the **group** of the directory.

Set SGID on directory:

```
chmod 2775 teamfolder
```

---

### **Sticky Bit**

Users can only delete **their own files** inside shared directories.

```
chmod 1777 /shared
```

You already know this directory:

```
/tmp  → drwxrwxrwt
```

The **t** represents sticky bit.

---

# ⭐ **8. ACL (Access Control List) — Advanced Permissions**

ACLs allow giving permissions to **specific users or groups** beyond the standard model.

### Check ACL:

```
getfacl file
```

### Add ACL:

```
setfacl -m u:john:r file
```

Give **read** permission to user john.

### Add ACL for directory:

```
setfacl -m u:sara:rw /project
```

### Remove ACL:

```
setfacl -x u:john file
```

### Default ACL for new files:

```
setfacl -m d:u:john:rw /project
```

---

# ⭐ **9. umask — Default File Permission Mask**

Check umask:

```
umask
```

Default in most systems:

```
022
```

Meaning:

* Files get 644
* Folders get 755

---

# 🧪 **DAY 4 Practice Tasks (Do These in Your VM)**

### **Task 1: Create folder and control permissions**

```
mkdir day4
cd day4
touch file1
chmod 644 file1
ls -l
```

### **Task 2: Change ownership**

```
sudo chown root:root file1
```

### **Task 3: Set ACL**

```
setfacl -m u:student:rwx file1
getfacl file1
```

### **Task 4: Apply sticky bit**

```
mkdir /tmp/shared
chmod 1777 /tmp/shared
ls -ld /tmp/shared
```

### **Task 5: Test umask**

```
umask 022
touch test1
ls -l test1
```


# 👉 Ready for **DAY 5: User & Group Management (useradd, passwd, usermod, /etc/passwd, /etc/shadow, sudoers)?**
