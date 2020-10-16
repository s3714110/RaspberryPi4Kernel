
#   % build_kernel VERSION 1.0 | User Manuals                   


### **NAME**

   **build_kernel** - builds and installs kernal on a Raspberry Pi 4

### **SYNOPSIS**

    ./build_kernel [&]

### **DESCRIPTION**

   **build_kernel** is a script that builds and installs a customiomised kernel for your Raspberry Pi 4. This script also installs necessary packages for the kernal install and backs up 
     the current kernel in case something fails. While compiling the kernel, the script will also call first_perf_script, that measures CPU temperature and clock speeds every second and 
     outputs the data to an external file. After finishing installing the new kernel, the script will automatically reboot the system to load up the new kernel.
     
### **OPTIONS**

     &   Runs the script in the background
### **FILES**

      /workdir/kernel-backup.tar
          Backup of the current kernel module before installation.
	  
      /workdir/boot-backup.tar
          Backup of the current boot folder before installation.
	  
      .config
	  The configuation file for the new kernel. Some changes will be automatically made to the config file by the script.
	  
      ./first_perf_script
          Script that measures CPU temp and clock every second.

### **ENVIRONMENT**

     SUDO=/usr/bin/sudo
          Grants sudo access to perform elevated privileges.
     
     APT=/usr/bin/apt
          Used to install some of the prerequisite packages

     RM=/bin/rm
          Removes files or folders
     
     MKDIR=/bin/mkdir
          Makes new directory
     
     SED=/bin/sed
          A stream editor that was used to edit the .config file. 

     MAKE=/usr/bin/make
          Compiles files using a Makefile file. Was used to complie and install the kernel
     
     CP=/bin/cp
          Copies files and folders
     
     GIT=/usr/bin/git
          Invokes git program. Was used to checkout my own repository and the Raspberry Pi kernal repository
     
     BASH=/bin/bash
          Invokes bash to run a script
     
     PKILL=/usr/bin/pkill
          Used to kill a process using their name. It was also used to send a custom signal for other scripts

     TAR=/bin/tar
          Used to compress files and folder for easy storage
     
     UNAME=/bin/uname
          Prints system information
     
     REBOOT=/sbin/reboot
          Reboots the system

### **DIAGNOSTICS**

     Permission Denied
          This scripts contains some commands elevated privileges. Users need to have access to sudo command to run this script.

     Error when cloning raspberry pi kernel repository
          Because the kernal is quite heavy, it's very likely that you don't have enough space to download the content of the repository, so make sure you have enough disk space.

     NO SSH KEY FOUND FOR GITHUB.
          This is because you either have not added a SSH key pairto your account, or you have misplaced the SSH private key into the wrong folder. Please consult github documentation for more info.

     Error occured while compiling kernel
	  You might have a different Pi model. Please note this script contains config file for Raspberry 4 Pi model only.
	  
### **BUGS**

     No bugs have been found as of yet. Please contact the author if you find any bug within the script.

### **AUTHOR**

   Lam Tran 
   <s3714110@student.rmit.edu.au>

### **SEE ALSO**
   [first_perf_script](first_perf_script.md), [second_perf_script](second_perf_script.md)
