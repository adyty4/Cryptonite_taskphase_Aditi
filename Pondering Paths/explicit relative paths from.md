# explicit relative paths 
***
Connected to the host amd changed the directory to / then i entered ./challenge/run to establish the flag
***
Connected!
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ /challenge/run
Incorrect...
You invoked this challenge with an absolute path. This challenge needs a relative path!
hacker@paths~explicit-relative-paths-from-:/$ .challenge/run
ssh-entrypoint: .challenge/run: No such file or directory
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{wZbQrdXrvIIGWsDgeaY8WyS0a9-.dBTN1QDL4YzN1czW}
***
 Resources used:
 Dojo
