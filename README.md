
#   build_kernel(1) | User Manuals                   


### **NAME**

   **build_kernel** - builds and installs kernal on a Raspberry Pi 4

### **SYNOPSIS**

    ./build_kernel [&]

### **DESCRIPTION**

   **build_kernel** is a script that builds and installs a customiomised kernel for your Raspberry Pi 4. This script also installs necessary packages for the kernal install and backs up 
     the current kernel in case something fails. While compiling the kernel, the script will also call first_perf_script, that measures CPU temperature and clock speeds every second and 
     outputs the data to an external file. After finishing installing the new kernel, the script will automatically reboot the system to load up the new kernel.
     
### **OPTIONS**

     &   Runs the script in the background (not outputting to terminal).
### **FILES**

      /workdir/kernel-backup.tar
          Backup of the current kernel module before installation.
	  
      /workdir/boot-backup.tar
          Backup of the current boot folder before installation.
	  
      .config
	  The configuation file for the new kernel. Some changes will be automatically made to the config file by the script.
	  
      ./first_perf_script
          Script that measures CPU temp and clock every second.
      
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



