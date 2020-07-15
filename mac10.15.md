Install gdb on your mac 
1. Open terminal 
2. Type in "brew install gdb"
3. To check the software edition: gdb -v

Installtion for adding certificate can be find from 
https://gist.github.com/gravitylow/fb595186ce6068537a6e9da6d8b5b96d


Some issues I have encountered: 

1. [New Thread 0xd03 of process 1661]
 Solution: 

 Control + Z to quit the program you are currently running  
 Type in the code below: 

 touch ~/.gdbinit
 echo "set startup-with-shell off" >> ~/.gdbinit

2. Unable to find Mach task port for process-id 919: (os/kern) failure (0x5).
 (please check gdb is codesigned - see taskgated(8))
 
 Solution: sudo gdb executableFileName (add sudo) 
 
 
 Hope this helps!! 
