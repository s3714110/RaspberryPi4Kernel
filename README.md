
#   Assignemt 2, Unix Systems Administration and Programming


  This repository contains scripts and documentations for Assignment 2, along with performance data and charted generated by the script.

  To run this script, simply run this command in your terminal

	./build_kernel

  This script is specifically configured for Raspberry Pi 4 model, so if you have a Pi 2 or 3, please refer to the **Modify config** section below 

### **USER DOCUMENTATION**

  [build_kernel()](build_kernel.md)

  [first_perf_script()](first_perf_script.md)


### **MODIFY CONFIG**

  To run this script on a Raspberry Pi 2 and 3 model, open **build_kernel** file with a text editor, find these lines
	
	KERNEL=kernel7l
	$MAKE bcm2711_defconfig
  
  And replace it with these lines
	 
	KERNEL=kernel7
	make bcm2709_defconfig