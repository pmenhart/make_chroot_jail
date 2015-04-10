# make_chroot_jail
Script to easily setup a chroot jail for ssh / scp / sftp with Linux

The original commit contains unmodified copy of the script from  
http://www.fuschlberger.net/programs/ssh-scp-sftp-chroot-jail/  
You'll find nice explanation and usage instructions there.  
More specific examples are on the net, search for "make_chroot_jail".

Second commit has changes needed for Ubuntu 12.04, and was originally published at
http://www.devcu.com/forums/topic/560-chrootjail-users-for-sshscp-ubuntu-1204/

Finally, current version made the script non-interactive, better suitable for automated operation:
 * create user without a password
 * if the user exists and jailed then do nothing
 * if the user exists then jail her
 * do not create shell if already exists

Additional changes:
 * tested on Ubuntu 8.04 to 14.04
 * added APPS: cat more less nano
 * copied /lib/terminfo
