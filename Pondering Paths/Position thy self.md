# Position thy self
***
Connected to host and entered cd / to change directory to root directory and then entered /challenge/run through which i understood that the dictionary needed is tmp 
so after changing the directory to tmp under / it took me a few tries to figure out the correct command to establish the flag
***
Connected!
hacker@paths~position-thy-self:~$ cd /
hacker@paths~position-thy-self:/$ /challenge/run
Incorrect...
You are not currently in the /tmp directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:/$ /tmp
ssh-entrypoint: /tmp: Is a directory
hacker@paths~position-thy-self:/$ cd /tmp
hacker@paths~position-thy-self:/tmp$ /challenge
ssh-entrypoint: /challenge: Is a directory
hacker@paths~position-thy-self:/tmp$ challenge/run
ssh-entrypoint: challenge/run: No such file or directory
hacker@paths~position-thy-self:/tmp$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EOxVdHDyAdVZUvb2SmAnrbM88yn.dZDN1QDL4YzN1czW}
***
Resources used:
dojo
