# Help for Builtins
***
Connected to host and entered help challenge to look up help for the shell builtin challengethrough which i got the argument to be used, Then i simple changed the directory to /challenge and entered the agrument.
***
Connected!
hhacker@man~help-for-builtins:~$ help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "wP222oMT".
hacker@man~help-for-builtins:~$ cd /
hacker@man~help-for-builtins:/$ cd challenge
hacker@man~help-for-builtins:~$ /challenge --secret wP222oMT
ssh-entrypoint: /challenge: Is a directory
hacker@man~help-for-builtins:/challenge$ challenge --secret wP222oMT
Correct! Here is your flag!
pwn.college{wP222oMTPIG2zfgutbT594iJTKP.dRTM5QDL4YzN1czW}
***
Resources used:
Dojo
