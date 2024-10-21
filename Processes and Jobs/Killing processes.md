# Killing processes
***
Connected to host and then displayed the processes, then i identified the PID and killed it lastly i ran /challenge
***
Connected!
ps aux | grep dhacker@processes~killing-processes:~$ ps aux | grep dont_run
hacker        73  0.0  0.0   4976  3200 ?        Ss   19:54   0:00 /challenge/dont_run
hacker       110  0.0  0.0   4140  2240 pts/0    S+   19:54   0:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill grep --color=auto dont_run
ssh-entrypoint: kill: grep: arguments must be process or job IDs
ssh-entrypoint: kill: --color=auto: arguments must be process or job IDs
ssh-entrypoint: kill: dont_run: arguments must be process or job IDs
hacker@processes~killing-processes:~$ kill /challenge/dont_run
ssh-entrypoint: kill: /challenge/dont_run: arguments must be process or job IDs
hacker@processes~killing-processes:~$ kill 73
hacker@processes~killing-processes:~$ ps aux | grep dont_run
hacker       112  0.0  0.0   4140  2560 pts/0    S+   19:57   0:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{k2UTgqc7xXkUf30197xCDZeW9Gd.dJDN4QDL4YzN1czW}
***
Resources used:
Dojo
