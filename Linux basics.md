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

**RPM command**
   * To install a package : **rpm -ivh package.rpm**
   * To uninstall a package: **rpm -e package**
   * To upgrade an existing package:**rpm -Uvh package.rpm**
   * To query the RPM packages :**rpm -q package**
  
**YUM command**
   * To install a package : **yum install  package**
   * To remove a package: **yum remove packagename**
   * To upgrade an existing package:**yum update package**
   * To List the packages :**yum repolist**

**DPKG command**
   * To install a package : **dpkg  -i  packagename**
   * To remove a package: **dpkg -r packagename**
   * To List the packages : **dpkg -l**

**APT command**
   * To install a package : **apt install packagename**
   * To remove a package: **apt remove packagename**
   * To List the package : **apt search packagename**
   * To upgarde the packaes :**apt update packagename**
