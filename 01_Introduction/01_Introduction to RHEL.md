

# **📘 DAY 1 — Linux & RHEL Foundations (Beginner Friendly)**

---

# **1. What is Linux? (Simple Explanation)**

Linux is an **open-source operating system kernel** created by Linus Torvalds in 1991.

* The **kernel** is the core of the OS
* Developers take the kernel → add packages, software, updates → create **distributions (distros)**
* Distros = different flavours of Linux

Linux is widely used in:

* Servers
* Cloud (AWS, Azure, GCP)
* DevOps
* Cybersecurity
* Networking
* Supercomputers
* IoT devices

---

# **2. What is RHEL? (Red Hat Enterprise Linux)**

RHEL = **enterprise-grade**, commercial Linux distribution developed by **Red Hat (owned by IBM)**.

✔ Stable
✔ Secure
✔ Long-term support
✔ Certified for enterprises
✔ Used heavily in production servers
✔ Comes with support, patches, updates, security fixes

RHEL is popular in:

* Banks
* Government
* Cloud infrastructure
* Big enterprises
* Large networks
* Data centers

---

# **3. Popular Linux Distributions (Types of Linux)**

### ✔ **RPM-based (Red Hat family)**

* RHEL (Red Hat Enterprise Linux)
* CentOS
* Fedora
* Rocky Linux
* AlmaLinux
* Oracle Linux

### ✔ **Debian-based**

* Debian
* Ubuntu
* Linux Mint
* Kali Linux

### ✔ **Other Distros**

* Arch Linux
* SUSE Linux Enterprise (SLES)
* Manjaro
* Gentoo

---

# **4. Is RHEL Free? Why CentOS Was Required?**

### ✔ **Is RHEL free?**

* **Officially RHEL is NOT free** because it comes with **paid support**.
* But Red Hat offers **Developer Subscription = FREE RHEL for personal learning**.

You can download free RHEL from:
👉 *Red Hat Developer Program*

### ✔ Then why was CentOS required?

Earlier:

* RHEL source code is open (because Linux is open-source).
* But RHEL itself required paid licenses.

So community created:

### **CentOS = a free rebuild of RHEL without Red Hat branding or support.**

It was binary-compatible with RHEL (same commands, same packages).
Companies used CentOS because:

* **Free RHEL alternative**
* **Stable**
* **Production-ready without support cost**

But Red Hat stopped CentOS Linux in 2020 and replaced it with:

* **CentOS Stream** = rolling, upstream version, not suitable for production

So alternatives emerged:

* **Rocky Linux**
* **AlmaLinux**
  These are 1:1 replacements for traditional CentOS.

---

# **5. Fedora, RHEL, CentOS — Relationship (Very Important)**

Think of it like this:

```
Fedora → RHEL → CentOS
(Upstream) (Enterprise) (Downstream)
```

### **Fedora**

* Cutting-edge
* Latest packages
* New features
  **Upstream** = development happens first in Fedora

### **RHEL**

* Stable
* Enterprise-ready
* Long-term support
  Fedora innovations → tested → become part of RHEL

### **CentOS (before 2020)**

* **Downstream rebuild** of RHEL
* Free clone
* Used when budget = low

Now replaced by:

* Rocky Linux
* AlmaLinux

---

# **6. How RHEL Is Different from Ubuntu (Debian-based)**

### **Package Manager**

| Feature         | RHEL (Red Hat)          | Ubuntu (Debian)        |
| --------------- | ----------------------- | ---------------------- |
| Package manager | **dnf / yum**           | **apt**                |
| Package format  | **.rpm**                | **.deb**               |
| Target          | **Enterprise, servers** | **Desktop + servers**  |
| Release cycle   | Slow, stable            | Faster updates         |
| SELinux         | Enabled by default      | AppArmor (less strict) |

---

# **7. If RHEL is so good, why do companies use Ubuntu?**

### ✔ Companies use Ubuntu because:

* Very easy & beginner friendly
* Fast installation and updates
* Huge community support
* Popular for **Developer machines**, cloud instances, DevOps
* Many modern tools (Docker, Kubernetes) are tested first on Ubuntu
* Free forever
* Lightweight for small-scale deployments

### ✔ RHEL is used when:

* Requires **certified environment** (Oracle DB, SAP, Banking applications)
* Needs **commercial support**
* High security & compliance
* Fortune 500 companies

**Both have their purpose.**

---

# **8. Minimum System Requirements for RHEL**

### ✔ **Minimum**

* 2 GB RAM
* 20 GB Disk
* 1 GHz CPU
* Internet optional

### ✔ **Recommended (for smooth learning)**

* **4–8 GB RAM**
* **30–50 GB disk**
* Dual-core or higher CPU
* VirtualBox / VMware

---

# **9. Do You Need GUI in RHEL?**

### ✔ **For learning: GUI is optional but helpful**

RHEL is mostly used in servers → **no GUI**, only terminal.

But as a beginner, GUI can help you understand:

* File system
* Network settings
* Tools

### ✔ So, recommendation:

* Start with **RHEL + GUI**
* After 1–2 weeks → switch to **RHEL minimal (No GUI)**
* Use terminal commands for everything

This builds true admin skills.

---

# **👍 Day 1 Homework**

To finish Day 1, you should be able to answer:

* What is Linux kernel?

  It is an open-source kernel developed by Linus Torvald.As previous version (UNIX) was not free he developed Linux which is open-source.
* What is RHEL used for?

  RHEL(Red Hat Enterprise Linux) is a distribution of Linux mainly used for testing purposes.
* Difference b/w RHEL, CentOS, Fedora

  RHEL-Mostly free but deamnds paid support
  CentOS-Exactly like RHEL but free branding and support
  Fedora-Used for testing purpose before updating or launching into RHEL or CentOS.
* RHEL vs Ubuntu

  Ubuntu has more faster installations and updates as compared to RHEL,free forever.
  RHEL is not free and comes with paid support and is slower as compared to Ubuntu.
* Do we need GUI?
  GUI is optional but is used mainly for tools and learning purposes.We use CLI mainly.
---

