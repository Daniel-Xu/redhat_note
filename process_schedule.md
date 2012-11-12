2012/06/04
- - - 
# process
 
  + check info
	
  	*static information*

    > ps aux

	*dynamic information*

	> top

  + find process Id
  
 	> pgrep  process_name

	> pgrep "init"

	*list process name which contains substring*

	*l ---> list*

	> pgrep -l "log"

	*U ---> user, t ---> console*

	> pgrep -l -U username -t tty1

  + process relationship

  	*a ---> all, u ---> user, p ---> pid*

	> pstree -aup

  + background process

  	*run in background*

  	> firefox bash.html &

	*pend in background*

	> ctrl-Z

	*switch jobs*
		
	> fg sequence_num 

	*show background process*	

	> jobs

  + kill

  	*stop process*

	*-9 force stopping*

    > kill -9 pid

	> killall -9 service_name

	*stop process according to condition*

    > pkill -9 -U "username"

# nice

  *adjust the priority of process*

  *range -20~19*

  > nice

  > nice -n -14 nice

  > nice --adjustment +20 nice 

# renice 

  *adjust the running process*
		
  *-p ---> pid, -g ---> group, -u ---> user*

  > renice -5 -p pid

# plan

  + at 

    + make schedule

      *at HH:MM  YYYY-MM-DD*

      > at 19:20 2012-06-09

	  *stop input* 

      > ctrl-D

    + show schedule

      > atq 

	+ remove plan

      *atrm seqence*

      > atrm 2

  + crontab

  	*min hour date mon week*

    + conf file

	  *global configure file*

	  > /etc/crontab

	  *service script*

	  > /etc/init.d/crond

	  *keep user's plan*

	  > /var/spool/cron/username
		
	  *set the authority of users, and allow is prior to deny*

	  > /etc/cron.allow

	  > /etc/cron.deny

	+ edit

	  *edit current user's plan*

	  > crontab -e

	  *edit specified user's plan*

	  > crontab -e -u user

	+ show

      > crontab -l

	+ delete
		
	  > crontab -r -u user

    + crontab form

	  ![Alt "charactor"](https://github.com/Daniel-Xu/redhat_note/raw/master/pic/charactor.jpg "charactor")
	
	+ example
	 
	  ![Alt "crond_exp"](https://github.com/Daniel-Xu/redhat_note/raw/master/pic/crond_exp.jpg "crond_exp")

    + save

	  > service crond restart

	  > chkconfig --level 35 crond on

	  or

	  > chkconfig crond on


