
#   first_perf_script() VERSION 1.0 | User Manuals                   


### **NAME**

   **first_perf_script** - measures ARM CPU temperature and clock speed every second

### **SYNOPSIS**

    ./first_perf_script [&]

### **DESCRIPTION**

   **first_perf_script** is a script that measures ARM CPU temperature and clock speed every second and outputs the result into an external file. The data file can then be graphed into a chart using external tools like gnuplot
     
### **OPTIONS**

     &   Runs the script in the background (not outputting to terminal).

### **FILES**

      kernel_performance_data
          The output data file of the script. The data format is tab-delimited.
	  
      
### **DIAGNOSTICS**

     Permission Denied
          This scripts contains some commands elevated privileges. Users need to have access to sudo command to run this script.

   
### **BUGS**

     No bugs have been found as of yet. Please contact the author if you find any bug within the script.

### **AUTHOR**

   Lam Tran 
   <s3714110@student.rmit.edu.au>

### **SEE ALSO**
   [build_kernel()](build_kernel.md)

