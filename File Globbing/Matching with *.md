# Matching with *
***
Connected to host and changed the directory to / then after a few attempts i entered cd /ch* to get the flag
***
Connected!
This challenge resets your working directory to /home/hacker unless you change
directory properly...
hacker@globbing~matching-with-:~$ cd /*
ssh-entrypoint: cd: too many arguments
hacker@globbing~matching-with-:~$ cd /
hacker@globbing~matching-with-:/$ cd *halle*nge
You specified the path to 'cd' to in more than 4 characters. Disallowed!
hacker@globbing~matching-with-:/$ cd *hall
You specified the path to 'cd' to in more than 4 characters. Disallowed!
hacker@globbing~matching-with-:/$ cd ch*l
ssh-entrypoint: cd: ch*l: No such file or directory
hacker@globbing~matching-with-:/$ cd challenge
You specified the path to 'cd' to in more than 4 characters. Disallowed!
hacker@globbing~matching-with-:/$ cd /*
ssh-entrypoint: cd: too many arguments
hacker@globbing~matching-with-:/$ cd *
ssh-entrypoint: cd: too many arguments
hacker@globbing~matching-with-:/$ cd /ch*
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{kwxp3NCtdcmLl_4Ufv7mTSIkjvm.dFjM4QDL4YzN1czW}
***
Resources used:
Dojo
