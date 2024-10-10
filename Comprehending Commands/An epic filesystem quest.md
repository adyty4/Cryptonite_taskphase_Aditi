# An epic filesystem quest
***
Connected to the host and changed to root directory. Then i listed the files of the directory, read the one of the files and then just followed the clues to establish the flag
***
Connected!
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
INSIGHT  boot       dev  flag  lib    lib64   media  nix  proc  run   srv  tmp  var
bin      challenge  etc  home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~an-epic-filesystem-quest:/$ ls -a
.   .dockerenv  bin   challenge  etc   home  lib32  libx32  mnt  opt   root  sbin  sys  usr
..  INSIGHT     boot  dev        flag  lib   lib64  media   nix  proc  run   srv   tmp  var
hacker@commands~an-epic-filesystem-quest:/$ cat flag
cat: flag: Permission denied
hacker@commands~an-epic-filesystem-quest:/$ cat INSIGHT
Tubular find!
The next clue is in: /opt/linux/linux-5.4/drivers/pci/endpoint

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/$ cd /opt/linux/linux-5.4/drivers/pci/endpoint
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ ls
BRIEF  Kconfig  Makefile  functions  pci-ep-cfs.c  pci-epc-core.c  pci-epc-mem.c  pci-epf-core.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cat BRIEF
Lucky listing!
The next clue is in: /usr/share/racket/pkgs/html-doc/html/compiled

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ ls /usr/share/racket/pkgs/html-doc/html/compiled
CLUE-TRAPPED  html_scrbl.dep  html_scrbl.zo  info_rkt.dep  info_rkt.zo
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cat CLUE-TRAPPED
cat: CLUE-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ ls CLUE-TRAPPED
ls: cannot access 'CLUE-TRAPPED': No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cat /usr/share/racket/pkgs/html-doc/html/compiled
cat: /usr/share/racket/pkgs/html-doc/html/compiled: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cat /opt/linux/linux-5.4/drivers/pci/endpoint
cat: /opt/linux/linux-5.4/drivers/pci/endpoint: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cat /usr/share/racket/pkgs/html-doc/
html/compiled/CLUE-TRAPPED
Lucky listing!
The next clue is in: /opt/linux/linux-5.4/include/soc/tegra

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ ls
BRIEF  Kconfig  Makefile  functions  pci-ep-cfs.c  pci-epc-core.c  pci-epc-mem.c  pci-epf-core.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ grep . Brief
grep: Brief: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ grep . /functions
grep: /functions: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ grep . /opt/linux/linux-5.4/drivers/pci/endpoint
grep: /opt/linux/linux-5.4/drivers/pci/endpoint: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ ls -a
.  ..  BRIEF  Kconfig  Makefile  functions  pci-ep-cfs.c  pci-epc-core.c  pci-epc-mem.c  pci-epf-core.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cat . ..
cat: .: Is a directory
cat: ..: Is a directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ ls . ..
.:
BRIEF  Kconfig  Makefile  functions  pci-ep-cfs.c  pci-epc-core.c  pci-epc-mem.c  pci-epf-core.c

..:
Kconfig     controller     mmap.c             pci-bridge-emul.h  pci-sysfs.o  quirks.c     setup-bus.o  vc.c
Makefile    ecam.c         mmap.o             pci-driver.c       pci.c        quirks.o     setup-irq.c  vc.o
access.c    endpoint       msi.c              pci-driver.o       pci.h        remove.c     setup-irq.o  vpd.c
access.o    host-bridge.c  msi.o              pci-label.c        pci.o        remove.o     setup-res.c  vpd.o
ats.c       host-bridge.o  of.c               pci-label.o        pcie         rom.c        setup-res.o  xen-pcifront.c
ats.o       hotplug        p2pdma.c           pci-mid.c          probe.c      rom.o        slot.c
built-in.a  iov.c          pci-acpi.c         pci-pf-stub.c      probe.o      search.c     slot.o
bus.c       irq.c          pci-acpi.o         pci-stub.c         proc.c       search.o     switch
bus.o       irq.o          pci-bridge-emul.c  pci-sysfs.c        proc.o       setup-bus.c  syscall.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cat controller
cat: controller: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/pci/endpoint$ cd /opt/linux/linux-5.4/include/soc/tegra
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/soc/tegra$ ls -a
.  ..  .CUE  ahb.h  bpmp-abi.h  bpmp.h  common.h  cpuidle.h  emc.h  flowctrl.h  fuse.h  ivc.h  mc.h  pm.h  pmc.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/soc/tegra$ cat .CUE
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/drivers/media/rc

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/soc/tegra$ ls /opt/linux/linux-5.4/drivers/media/rc
EVIDENCE-TRAPPED  gpio-ir-recv.c     ir-mce_kbd-decoder.c  ir-xmp-decoder.c  pwm-ir-tx.c     sunxi-cir.c
Kconfig           gpio-ir-tx.c       ir-nec-decoder.c      ite-cir.c         rc-core-priv.h  tango-ir.c
Makefile          igorplugusb.c      ir-rc5-decoder.c      ite-cir.h         rc-ir-raw.c     ttusbir.c
ati_remote.c      iguanair.c         ir-rc6-decoder.c      keymaps           rc-loopback.c   winbond-cir.c
bpf-lirc.c        img-ir             ir-rcmm-decoder.c     lirc_dev.c        rc-main.c       xbox_remote.c
built-in.a        imon.c             ir-rx51.c             mceusb.c          redrat3.c       zx-irdec.c
ene_ir.c          imon_raw.c         ir-sanyo-decoder.c    meson-ir.c        serial_ir.c
ene_ir.h          ir-hix5hd2.c       ir-sharp-decoder.c    mtk-cir.c         sir_ir.c
fintek-cir.c      ir-imon-decoder.c  ir-sony-decoder.c     nuvoton-cir.c     st_rc.c
fintek-cir.h      ir-jvc-decoder.c   ir-spi.c              nuvoton-cir.h     streamzap.c
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/soc/tegra$ cat EVIDENCE-TRAPPED
cat: EVIDENCE-TRAPPED: No such file or directory
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/soc/tegra$ cat /opt/linux/linux-5.4/include/soc/tegra$ ls /opt/linux/linux-5.4/drivers/media/rc/EVIDENCE-TRAPPED
cat: '/opt/linux/linux-5.4/include/soc/tegra$': No such file or directory
cat: ls: No such file or directory
Great sleuthing!
The next clue is in: /opt/linux/linux-5.4/drivers/gpu/drm/nouveau/include/nvif

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/soc/tegra$ cd /opt/linux/linux-5.4/drivers/gpu/drm/nouveau/include/nvif
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/nouveau/include/nvif$ ls -a
.         cl006b.h  cl507a.h  cl826e.h  class.h   client.h  fifo.h    if0004.h  if000c.h  if900d.h  mem.h     unpack.h
..        cl0080.h  cl507b.h  cl826f.h  clb069.h  device.h  if0000.h  if0005.h  if000d.h  ifb00d.h  mmu.h     user.h
.MESSAGE  cl506e.h  cl507c.h  cl906f.h  clc36f.h  disp.h    if0001.h  if0008.h  if500b.h  ifc00d.h  notify.h  vmm.h
cl0002.h  cl506f.h  cl507d.h  cl9097.h  clc37b.h  driver.h  if0002.h  if000a.h  if500d.h  ioctl.h   object.h
cl0046.h  cl5070.h  cl507e.h  cla06f.h  clc37e.h  event.h   if0003.h  if000b.h  if900b.h  list.h    os.h
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/nouveau/include/nvif$ cat .MESSAGE
Great sleuthing!
The next clue is in: /opt/radare2/libr/arch/p/arm/v35/arch-arm64/.git/logs/refs/remotes

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/drivers/gpu/drm/nouveau/include/nvif$ cd /opt/radare2/libr/arch/p/arm/v35/arch-arm64/.git/logs/refs/remotes
hacker@commands~an-epic-filesystem-quest:/opt/radare2/libr/arch/p/arm/v35/arch-arm64/.git/logs/refs/remotes$ ls -a
.  ..  SECRET  origin
hacker@commands~an-epic-filesystem-quest:/opt/radare2/libr/arch/p/arm/v35/arch-arm64/.git/logs/refs/remotes$ cat SECRET
Tubular find!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/hush/bash/source
hacker@commands~an-epic-filesystem-quest:/opt/radare2/libr/arch/p/arm/v35/arch-arm64/.git/logs/refs/remotes$ cd /opt/busybox/busybox-1.33.2/include/config/hush/bash/source
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/hush/bash/source$ ls -a
.  ..  NOTE  curdir.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/hush/bash/source$ cat NOTE
Yahaha, you found me!
The next clue is in: /opt/busybox/busybox-1.33.2/include/config/feature/mkswap

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/hush/bash/source$ cd /opt/busybox/busybox-1.33.2/include/config/feature/mkswap
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/mkswap$ ls -a
.  ..  BLUEPRINT  uuid.h
hacker@commands~an-epic-filesystem-quest:/opt/busybox/busybox-1.33.2/include/config/feature/mkswap$ cat BLUEPRINT
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{05JdurueUf-jVYfeBIQiCzOiR7K.dljM4QDL4YzN1czW}
***
Resources used:
Dojo
