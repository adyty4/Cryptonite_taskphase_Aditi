# Reading manuals
***
Connected to host and then read the manual of challenge which gave the option to get the flag
***
hacker@man~reading-manuals:~$ man challenge

CHALLENGE(1)                                      Challenge Commands                                     CHALLENGE(1)

NAME
       /challenge/challenge - print the flag!

SYNOPSIS
       challenge OPTION

DESCRIPTION
       Output the flag when called with the right arguments.

       --fortune
              read a fortune

       --version
              output version information and exit

       --mdzrzh NUM
              print the flag if NUM is 848

AUTHOR
       Written by Zardus.

REPORTING BUGS
       The repository for this dojo: <https://github.com/pwncollege/linux-luminarium/>

SEE ALSO
       man(1) bash-builtins(7)
hacker@man~reading-manuals:~$ /challenge/challenge --mdzrzh 848
Correct usage! Your flag: pwn.college{848L5GmdPCAzrLzDIYh2BTn1MKq.dRTM4QDL4YzN1czW}
***
Resources used:
Dojo
