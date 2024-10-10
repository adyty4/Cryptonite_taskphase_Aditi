# hidden files
***
Connected to the host and firstly listed all the non hidden files and then listed with the hidden ones. lastly read the flag file to establish the flag
***
Connected!
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ ls -a
.   .dockerenv             bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-306733006722076  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:/$ cat .flag-306733006722076
pwn.college{MkCFj-8o2tyjRw40BMqUbGpET22.dBTN4QDL4YzN1czW}
***
Resources used
Dojo
