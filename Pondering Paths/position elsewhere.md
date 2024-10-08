# position elsewhere
***
Connected to host and then changed directory to / then i entered /challenge/run so the terminal would tell me the directory. Finally after changing the directory
to the said directory entered /challenge/run to establish the flag
***
Connected!
hacker@paths~position-elsewhere:~$ cd /
hacker@paths~position-elsewhere:/$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/$  /usr/aarch64-linux-gnu/include/gnu
ssh-entrypoint: /usr/aarch64-linux-gnu/include/gnu: Is a directory
hacker@paths~position-elsewhere:/$ cd ^C
hacker@paths~position-elsewhere:/$  /usr/aarch64-linux-gnu/include/gnu
ssh-entrypoint: /usr/aarch64-linux-gnu/include/gnu: Is a directory
hacker@paths~position-elsewhere:/$ /challenge/run
Incorrect...
You are not currently in the /usr/aarch64-linux-gnu/include/gnu directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:/$ cd /usr/aarch64-linux-gnu/include/gnu
hacker@paths~position-elsewhere:/usr/aarch64-linux-gnu/include/gnu$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{8tlmN30zEj53j0-UzjwxSqDRDPv.ddDN1QDL4YzN1czW}
***
Resources used:
Dojo
