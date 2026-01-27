# Linux Command Line Interface (CLI) Commands

## Basic Navigation
- `pwd` — Print current working directory
- `ls` — List directory contents
- `mkdir` — Create directory
- `rmdir` — Remove directory

## File & Directory Operations
- `touch` — Create empty file
- `cp` — Copy files/directories
- `mv` — Move/rename files/directories
- `rm` — Remove files/directories
- `cat` — Concatenate and display file content
- `less`, `more` — View file content page by page
- `head`, `tail` — View start/end of file
- `find` — Search for files/directories
- `grep` — Search text within files

## File Permissions & Ownership
- `chmod` — Change file permissions
- `chown` — Change file owner/group
- `sudo` — Execute command as superuser
- Understand the `rwx` permissions for user, group, and others

## Man Pages & Help
- `man <command>` — Manual page for command
- `<command> --help` — Command help

---

# File Types
In Linux, the phrase "everything is a file" reflects the idea that every object is represented as a file.
- **Regular Files** (`-`)
- **Directories** (`d`)
- **Special Files**:
   - Character Files (`c`)
   - Block Files (`b`)
   - Links (`l`)
      - Hard Links
      - Symbolic Links
   - Sockets (`s`)
   - Named Pipes (`p`)

---

# Package Management
Linux package management tools used across various Linux distributions:

## Types of Package Managers
- **DPKG** (Debian Package Manager)
- **APT** (Advanced Package Tool)
- **APT-GET**
- **RPM** (Red Hat Package Manager)
- **YUM** (Yellowdog Updater Modified)
- **DNF**

### RPM Commands
- Install a package: `rpm -ivh package.rpm`
- Uninstall a package: `rpm -e package`
- Upgrade an existing package: `rpm -Uvh package.rpm`
- Query RPM packages: `rpm -q package`

### YUM Commands
- Install a package: `yum install package`
- Remove a package: `yum remove packagename`
- Upgrade an existing package: `yum update package`
- List packages: `yum repolist`

### DPKG Commands
- Install a package: `dpkg -i packagename`
- Remove a package: `dpkg -r packagename`
- List packages: `dpkg -l`

### APT Commands
- Install a package: `apt install packagename`
- Remove a package: `apt remove packagename`
- List packages: `apt search packagename`
- Upgrade packages: `apt update packagename`

---

# File Commands
## View File Sizes
- `du -sk filename` — Shows file size in kilobytes
- `du -sh filename` — Shows file size in MB
- `ls -lh filename` — Shows file size in MB

---

# Archival File Commands
The `tar` command is commonly used to group multiple files:
- Create a tar archive: `tar -cf test.tar file1 file2 file3`
- View contents of tar: `tar -tf test.tar`
- Extract files: `tar -xf test.tar`
- Create compressed tar: `tar -zcf test.tar file1 file2 file3`

---

# File Search Commands
- Locate file quickly: `locate filename`
- Find file in directory: `find directorypath filename`
- Search text within files: `grep texttofind filename`

---

# Vi Editor Commands
- Save: `:w`
- Quit: `:q`
- Save & Quit: `:wq`
- Force Quit: `:q!`
- Copy a line: `yy`
- Delete a line: `dd`
- Paste: `p`
- Delete single character: `x`
## Linux Command Line Interface (CLI) commands 

* **Basic Navigation**: pwd, ls,  mkdir, rmdir.
   * pwd  Represent current working directory

* **File & Directory Operations**: touch, cp, mv, rm, cat, less, more, head, tail, find, grep.

* **File Permissions & Ownership**: chmod, chown, sudo. Understand the rwx permissions for user, group, and others.

 * **Man Pages & Help**: man <command>, <command> --help

# File Types
In Linux, the phrase "everything is a file" reflects the idea that every object.
   * Regular Files(-)
   * Directories(d)
   * Special Files
       *  Character Files(c)
       *  Block Files(b)
       *  Links(l)
            *  Hard Links
            *  Symbolic Links
       *  Sockets(s)
       *  Named Pipes(p)
         
# Package Management 
Linux package management tools used across various Linux distributions

**Types of Package**
 * DPKG (Debian Package Manager)
 * APT (Advanced Package Tool) 
 * APT-GET
 * RPM (Red Hat Package Manager)
 * YUM (Yellowdog Updater Modified)
 * DNF

**RPM commands**
   * To install a package : **rpm -ivh package.rpm**
   * To uninstall a package: **rpm -e package**
   * To upgrade an existing package:**rpm -Uvh package.rpm**
   * To query the RPM packages :**rpm -q package**
  
**YUM commands**
   * To install a package : **yum install  package**
   * To remove a package: **yum remove packagename**
   * To upgrade an existing package:**yum update package**
   * To List the packages :**yum repolist**

**DPKG commands**
   * To install a package : **dpkg  -i  packagename**
   * To remove a package: **dpkg -r packagename**
   * To List the packages : **dpkg -l**

**APT commands**
   * To install a package : **apt install packagename**
   * To remove a package: **apt remove packagename**
   * To List the package : **apt search packagename**
   * To upgarde the packaes :**apt update packagename**

**File Commands**
   * To View the files
       * du -sk filename   It will shows the file size in kilobytes
       * du -sh filename   It will shows the file size in MB
       * ls -lh filename    It will shows the file size in MB
    
 **Archival Files Commands**
   * The tar command is one of the most common utilities used to group multiple files
        * tar -cf test.tar file1 file2 file3     Its used to create a tar archive
        * tar -tf test.tar                       Its used to view the content of the tar
        * tar -xf test.tar                       Its used to extract files
        * tar -zcf test.tar file1 file2 file3    Its used to reduce its file size
    
 **File Search commands**
       * To locate file fast - locate filename.
       * To fine the in directory  - find directorypath filename
       * searching text within files -grep texttofind filename

**Vi Editor Commands**
   * Save  :w
   * Quit  :q
   * Save & Quit :wq
   * Quit :q!
   * copy a line -yy
   * delete -dd
   * paste -p
   * single character delete x
  
**Networking Commands**
  * Lists and modifies host interfaces : ip link
  * Displays IP addresses              : ip addr
  * Assigns an IP address              : Ip addr add
  * Views the routing table            : ip route 
  * Adds a new entry to the routing table : ip route add


      
       
       
   
