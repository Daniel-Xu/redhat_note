2012/06/04
- - - 
# quota

  *quota is just aimed at disk partition*

  + /etc/fstab

  	*edit the conf file to support quota*

	> device_name mount_path filesystem mount_attribution bak check_when_start

    > /dev/sdb1 /mailbox ext4 default,usrquota,grpquota 0 0

  + mount 

	*remount the device in /etc/fstab*
		
  	> mount -a

  + create quota file 

  	*run this command until the directory generates quota file*

	*u ---> user, g ---> group, c ---> creat, v ---> verbose information*

    > quotacheck -ugcv /dev/sdb1

	> ![Alt check](https://github.com/Daniel-Xu/redhat_note/raw/master/pic/quota_check.jpg "check")

  + add user
  
    > useradd alice

	> passwd alice

  + edit quoat file (user and group)

	*soft hard (KB)*

    > edquota -u username

	> ![Alt edit](https://github.com/Daniel-Xu/redhat_note/raw/master/pic/quota_edit.jpg "edit")

	> edquota -g groupname

  + active quota

  	*a ---> all, v ---> verbose, u ---> user, g ---> group*

  	> quotaon -avug

  + check whether succeed
  
	*if ---> read from file instead of stdin*  	

	*of ---> write to file instead of stdout*

	*bs ---> byte a time*

  	> dd if=/dev/zero of=myfile bs=1M count=120

	*This command generates a file of 120M*

  + show usage information

  	*show the user quota*

  	> quota -u alice

	> ![Alt user](https://github.com/Daniel-Xu/redhat_note/raw/master/pic/quota.jpg "quota -u")

	*report for user quotas on device (disk partition)*

	> repquota -a

	> ![Alt report](https://github.com/Daniel-Xu/redhat_note/raw/master/pic/repquota.jpg "report quota")

