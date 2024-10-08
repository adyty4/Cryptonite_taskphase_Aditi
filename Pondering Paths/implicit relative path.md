# implicit relative path .
***
Connected to host and changed the directory to / after which the terminal asked me to change to challenge directory. lastly i entered ./run to establish the flag
***
Connected!
hacker@paths~implicit-relative-path:~$ cd /
hacker@paths~implicit-relative-path:/$ ./challenge/run
Incorrect...
You are not currently in the /challenge directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-path:/$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{YO7oNBUL7Jxtb7Tl7xmRhZW087O.dFTN1QDL4YzN1czW}
***
 Resources used:
 Dojo
