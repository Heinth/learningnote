# Password reset for root

append "rd.break" in line start of linux&#x20;

mount -o remount,rw /sysroot&#x20;

chroot /sysroot passwd&#x20;

touch /.autorelabel

if ./autorelabel forget, edit append enforcing=0 in line start of linux
