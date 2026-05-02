### 🐧Linux Directory Structure (Hierarchy) ###

🌳 Overall structure:

```
/
├── bin

├── boot

├── dev

├── etc              

├── home            

├── lib

├── media

├── mnt

├── opt

├── proc

├── root

├── sbin

├── tmp

├── usr

└── var             
```

👉 ``/`` = root directory (top level)

Everything starts from here.

**Important Directories:**

### 🔹 ``/bin`` (Binary) ###

👉 Essential commands for all users

Examples:

```
ls, cp, mv, cat
```

### 🔹``/sbin`` (System Binary) ###

👉 Admin commands (root user)

```
reboot, shutdown, ifconfig
```

### 🔹``/etc`` (Configuration) ###

👉 All config files stored here

Example:

```
/etc/passwd
/etc/ssh/sshd_config
```
“Everything configuration = etc”

### 🔹 ``/home`` ###

👉 Home directory of root user

### 🔹 ``/var`` (Variable data) ###

👉 Logs, runtime data

```
/var/log
/var/lib
```

Example:

MySQL data → ``/var/lib/mysql``

Logs       → ``/var/log``

### 🔹 ``/tmp`` ###

👉 Temporary files

Auto deleted after reboot

### 🔹 ``/usr`` ###

👉 User programs & applications

```
/usr/bin
/usr/lib
```

“Installed software lives here”

### 🔹 ``/opt`` ###

Example:

```
/opt/app
```

### 🔹 ``/boot`` ###

👉 Boot files (kernel, init)

### 🔹 ``/dev`` ###

👉 Device files

Example:

```
/dev/sda
/dev/null
```

### 🔹 ``/proc`` ###

👉 System/process info (virtual)

### 🔹 ``/mnt & /media`` ###

👉 Mount points

``/mnt``  → manual mounts

``/media``  → USB/CD

**Easy Memory Trick**

```
"/" = root

etc  → configs  

var  → logs/data  

home → users  

bin  → commands  

opt  → apps  

tmp  → temp files
```

**👉 “Linux hierarchy starts from root (/) and organizes system files into directories like /etc for configs, /var for logs, /home for users, and /usr for applications.”**


