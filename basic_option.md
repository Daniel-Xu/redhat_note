#system info
	
> hostname
	
# vmware tool

  *This tool makes it easy for file transporting between Linux and Windows*

  > press **VM** and select install vmware tool

  > ![Alt vmware](/home/iverson/redhat_note/pic/basic_vmware.jpg "vmware tool")

  > umount /dev/cdrom

  > cd /media

  > cp vmwaretool /home/iverson/

  > tar -zvxf vmwaretool

  > cd vmwaretool

  > perl install.pl

# no login

  *This is used to manage services*

  > /sbin/nologin

# default runlevel
	
  > 0	halt

  > 1	single user mode

  > 2	Multiuser

  > 3	full multiuser

  > 4	unused

  > 5	X11

  > 6	reboot

# show service runlevel

  > chkconfig --list
	
# show current level
	
  > runlevel

# change service runlevel

  > chkconfig --level n service_name off/on

  > chkconfig --level 3 sshd on

	
