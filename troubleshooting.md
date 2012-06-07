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

