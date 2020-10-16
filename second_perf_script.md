
#   second_perf_script VERSION 1.0 | User Manuals                   


### **NAME**

   **second_perf_script** - changes the flicker frequency of the green LED to the CPU usage

### **SYNOPSIS**

    ./second_perf_script [&]

### **DESCRIPTION**

   **second_perf_script** is a script that measures the CPU usage and adjust the green LED to flicker accordingly. For example, if the CPU is  20% load then the LED will be on for one fifth of that second.
     
### **OPTIONS**

     &   Runs the script in the background

### **FILES**
    
      /sys/class/leds/led0/trigger
          This file is used to determine what triggers the green LED. The default value is "mmc0", which is SD card activity. 

      /sys/class/leds/led0/brightness
          This file is used to turn on or off the green LED. The value of this file can either be 1 or 0. This value will only last if the value of trigger file is "none"

### **ENVIRONMENT**

     SUDO=/usr/bin/sudo
          Grants sudo access to perform elevated privileges.
     
     TOP=/usr/bin/top
          Displays all processes and CPU usage. This was used to get the percentage of CPU usage
     
     TEE=/usr/bin/tee
          Reads from input and writes to a file. This was used to write to files that control the green LED
      
     BC=/usr/bin/bc
          An arbitrary precision calculator language. This was used to accurately calculate CPU usage, amount of time needed, since shell doesn't support floating numbers

     GREP=/bin/grep
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
   [build_kernel](build_kernel.md), [first_perf_script](first_perf_script.md)

