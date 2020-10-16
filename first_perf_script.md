
#   first_perf_script VERSION 1.0 | User Manuals                   


### **NAME**

   **first_perf_script** - measures ARM CPU temperature and clock speed every second

### **SYNOPSIS**

    ./first_perf_script [&]

### **DESCRIPTION**

   **first_perf_script** is a script that measures ARM CPU temperature and clock speed every second and outputs the result into an external file. The data file can then be graphed into a chart using external tools like gnuplot
     
### **OPTIONS**

     &   Runs the script in the background

### **FILES**

      kernel_performance_data
          The output data file of the script. The data format is tab-delimited.
	  
### **ENVIRONMENT**

     SUDO=/usr/bin/sudo
          Grants sudo access to perform elevated privileges.
     
     RM=/bin/rm
          Removes files or folders
     
     VCGENCMD=/usr/bin/vcgencmd
          Gets info of the machine's processor. Was used to get CPU temperature and clock speed
      
     AWK=/usr/bin/awk
          Writes to a file with options to format it. This was used to write data to the kernel_performance_data file

     EGREP=/bin/egrep
          Matches a word with a pattern using regex. This was used to clean up the performance data.

     CUT=/usr/bin/cut
          Cuts a line into parts with a delimitor. This was also used to clean up the performance data.

     SLEEP=/bin/sleep
          Puts the script into sleep for a defined amount of time
      
### **DIAGNOSTICS**

     Permission Denied
          This scripts contains some commands elevated privileges. Users need to have access to sudo command to run this script.

   
### **BUGS**

     No bugs have been found as of yet. Please contact the author if you find any bug within the script.

### **AUTHOR**

   Lam Tran 
   <s3714110@student.rmit.edu.au>

### **SEE ALSO**
   [build_kernel](build_kernel.md), [second_perf_script](second_perf_script.md)

