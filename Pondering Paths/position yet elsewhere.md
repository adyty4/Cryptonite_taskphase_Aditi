# position yet elsewhere
***
Connected to host and then changed directory to / then i entered /challenge/run so the terminal would tell me the directory. Finally after changing the directory
to the said directory entered /challenge/run to establish the flag
***
Connected!
hacker@paths~position-yet-elsewhere:~$ cd /
hacker@paths~position-yet-elsewhere:/$ /challenge/run
Incorrect...
You are not currently in the /proc/101 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:/$ cd /proc/101 directory
ssh-entrypoint: cd: too many arguments
hacker@paths~position-yet-elsewhere:/$ cd /proc/101
hacker@paths~position-yet-elsewhere:/proc/101$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{AbR25AqI9ZszPzrCjJK9Fdg-Sug.dhDN1QDL4YzN1czW}
***
Resouces used:
Dojo
