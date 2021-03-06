# Contiguous Memory Allocation Simulation


This program simulates three Contiguous Memory Allocation algorithms given a file that contains a list of memory allocation jobs and outputs if it succeeded or failed with the request that failed and the external fragmentation.

- First Fit Memory Allocation, Best Fit Memory Allocation, Worst Fit Memory Allocation

To compile this simulator you need to be in the directory of project java files and makefile, then type “make” into the command line. This will compile the MMDriver.java for you so you can run it.

To run the program:

Type into the command line “java MMDriver {name of memory file to simulate} “

For example, there are two text files as examples included in the folder.

This is how you would type them:

“java MMDriver MemJob0.txt” and “java MMDriver MemJob1.txt”

After the simulation has ended it should output the following for example if it failed:

----------First Fit----------
Request 21 failed at allocating 25 bytes.
External Fragmentation is 83 bytes.

----------Best Fit----------
Request 21 failed at allocating 25 bytes.
External Fragmentation is 83 bytes.

----------Worst Fit----------
Request 20 failed at allocating 21 bytes.
External Fragmentation is 104 bytes.

If the run succeeded it will output for example :

----------First Fit----------
Success

----------Best Fit----------
Success

----------Worst Fit----------
Success



# Format of File Argument

Example

1 1 30
<br/>
2 1 40
<br/>
3 1 50
<br/>
4 2 1


The first number is the reference id of job.
The second number is a request to allocate or deallocate. (1 - Allocate, 2 - Deallocate)
The third number if allocate will try and allocate those amount of bytes into a memory stack of 1024 bytes.
  If it is deallocate, the third argument will be the reference id to deallocate from memory.
  
There should be a space between each number


If for any reason it cannot read the file or the jobs into the simulator, the simulator will not run. A reason for this would be having a newline at the end of the file. It does not error check for this.
