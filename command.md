2012/05/21
- - - 

# du

  *show the size of each file in the directory*

  *s ---> sum, h ---> easy to read*

  > du -sh /home

  > du -sh /*

# df

  *Actual disk usage*
		
# ln

  + setup soft link

	> ln -s /etc/sysconfig/network-scripts/ifcfg-eth0 /etc/

  + setup hard link

	> ln /usr/sbin/system-config-network /sbin/netconfig

  + show soft link

	> ll name

  + show hard link  

    *we can check the inode of the file, they should be the same*

	> ls -ih name1 name2

# file

  *show the file type*

  > file /etc/fstab

# which

  *This command is always used to find the absolute path*

  > which commandname

# find

  + -name

	> find /etc -name "resolv\*.conf"

  + -size

	> find /boot -size +1024k -name "vmware"

  + -user

  + -type

	> find /boot -type d

  + -exec

    *`{}` refers to the result of the find*

    *`\`  is a must.*

	*result of commmand before the -exexc will act as the input of the command after it*

	> find /ect -name "passwd" -exec grep "root" {} \;

	*copy directories which contain /iveson to /opt*

	> find / -name iverson -exec cp -r {} /opt \;

# locate

  + usage

    *we always use locate to search some files, because it seems to be faster!*

	> locate $filename

  + update

    *sometimes we could not find the file existed, to solve the problem, we should do this:*

 	> updatedb

# compress

  + gzip

	> gzip -9 filename

  + bzip2

	> bzip2 -9 filename

# uncompress

  + gzip

	> gzip -d filename

  + bzip2

	> bzip2 -d filename

# package 
	
  + tar.gz

  	*take care of the sequence*

	*f ---> file, v ---> verbose, z ---> gz*

	> tar -czvf  name.tar.gz name

	> tar -xzvf 

  + bzip2

	*j ---> bzip2*

	> tar -xjvf




