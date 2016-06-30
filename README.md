# NYU Mathematics society website

This website is built with [jemdoc](http://jemdoc.jaboc.net/) (in particular, 
[jemdoc+MathJax](http://www.mit.edu/~wsshin/jemdoc+mathjax.html)) and 
[Travis-CI](https://travis-ci.org/).

## To edit

To edit the page index.html, click on index.jemdoc above and edit with Github's 
built in editor. Your changes will then automatically be copied and should show 
up online within a few minutes.

# Setup

To get this working on a new server:
1. Install the Travis command line tool
2. Run
```travis encrypt FTP_USER=user```
```travis encrypt FTP_PASSWORD=password```
```travis encrypt FTP_DIR=dir```
where `user` and `password` are your ftp username and password, respectively, 
and `dir` is the directory to install the website.

Copy the output of all 3 commands into `.travis.yml`, replacing the existing 
secure variables.

# To do

- Finish setup instructions
- Get deploy working: how to curl the whole build directory?
