# Searching Manuals
***
Connected to host and then opened the manual challenge. Then i searched argument related to flag using /flag ,lastly i entered the path and argument to get the flag.
***
Connected!
hacker@man~searching-manuals:~$ man challenge
hacker@man~searching-manuals:~$ /challenge/challenge/--ee
ssh-entrypoint: /challenge/challenge/--ee: Not a directory
hacker@man~searching-manuals:~$ cd / challenge
ssh-entrypoint: cd: too many arguments
hacker@man~searching-manuals:~$ cd/challenge
ssh-entrypoint: cd/challenge: No such file or directory
hacker@man~searching-manuals:~$ cd /
hacker@man~searching-manuals:/$ cd challenge
hacker@man~searching-manuals:/challenge$ cd /challenge
hacker@man~searching-manuals:/challenge$ / --ee
ssh-entrypoint: /: Is a directory
hacker@man~searching-manuals:/challenge$ --ee
ssh-entrypoint: --ee: command not found
hacker@man~searching-manuals:/challenge$ /challenge/challenge --ee
Initializing...
Correct usage! Your flag: pwn.college{kPj6iO5vAJVXgkTC351xpd1CPX0.dVTM4QDL4YzN1czW}
***
Resources used:
Dojo
