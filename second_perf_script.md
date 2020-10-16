
#   second_perf_script VERSION 1.0 | User Manuals                   


### **NAME**

   **second_perf_script** - changes the flicker frequency of the green LED to the CPU usage

### **SYNOPSIS**

    ./second_perf_script [&]

### **DESCRIPTION**

   **second_perf_script** is a script that measures the CPU usage and adjust the green LED to flicker accordingly. For example, if the CPU is  20% load then the LED will be on for one fifth of that second.
     
### **OPTIONS**

     &   Runs the script in the background (not outputting to terminal).

### **FILES**
    
      /sys/class/leds/led0/trigger
          This file is used to determine what triggers the green LED. The default value is "mmc0", which is SD card activity. 

      /sys/class/leds/led0/brightness
          This file is used to turn on or off the green LED. The value of this file can either be 1 or 0. This value will only last if the value of trigger file is "none"
      
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

