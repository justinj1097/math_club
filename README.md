# NYU Mathematics society website

This website is built with [jemdoc](http://jemdoc.jaboc.net/) (in particular, 
[jemdoc+MathJax](http://www.mit.edu/~wsshin/jemdoc+mathjax.html)) and 
[Travis-CI](https://travis-ci.org/).

## To edit

To edit the page index.html, click on index.jemdoc above and edit with Github's 
built in editor. Your changes will then automatically be copied and should show 
up online within a few minutes.

# Setup

Perform the following steps on your local machine:

1. Install the [Travis client](https://github.com/travis-ci/travis.rb#readme)
2. Run the following commands
	a. Generate a new encryption key pair so Travis can securely 
	communicate with your server
	```
	ssh-keygen -t rsa -b 4096 -C '<repo>@travis-ci.org' -f ./deploy_rsa
	```
	b. Encrypt the private key with Travis so it can be stored on Github
	```
	travis encrypt-file deploy_rsa --add
	```
	c. Add the public key to the server (replace <ssh-user> and 
	<deploy-host>):
	```
	ssh-copy-id -i deploy_rsa.pub <ssh-user>@<deploy-host>
	```
	d. Delete the key pair just in case
	```
	rm -f deploy_rsa deploy_rsa.pub
	```

# To do

- Convert setup instructions to setup script
- Get rsync to work
