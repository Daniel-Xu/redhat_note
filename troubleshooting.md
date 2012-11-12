# git install

  + first
    
    we should ensure that curl-devel package is installed in our computer

	otherwise, "fatal: Unable to find remote helper for 'https'" will occur.

  + second

  	install source code.

		1. ./configure

		2. make
	
		3. make install

  + third

    we should close ssl verify, otherwise, you can not push data to server.

	To do this:
    
	`$ git config --global http.sslVerify false`

# git image path
   
  In the markdown file in local computer,  picture path should be written like this:

  > `![Alt desc](/pic_dir_path/pic_name.jpg "desc")`

  However, we we `git push` this file, picture in the file can not display regularly

  To solve the problem, we should use raw format path, like this:

  > `![Alt desc](https://github.com/username/reponame/raw/branch/pic_dir/pic_name.jpg "desc")`

  > for a instance, like this
  
  > `![Alt desc](https://github.com/Daniel-Xu/redhat_note/raw/master/pic/pic_name.jpg "desc")`





