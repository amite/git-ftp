INSTALL
=======

Stable on Linux/Unix based systems using make
---------------------------------------------

Note: Make sure Git and cURL is installed.

This should work on Mac OS X, Debian, Ubuntu, Fedora, RedHat, etc.

The easiest way is to use Git for installing:

	$ git clone http://github.com/resmo/git-ftp.git
	$ cd git-ftp
	$ git checkout master
	$ sudo make install

Updating using git

	$ git pull
	$ sudo make install


Debian official
---------------
See http://packages.qa.debian.org/g/git-ftp.html


Ubuntu official
---------------
See https://launchpad.net/ubuntu/+source/git-ftp


Ubuntu PPA (Personal Package Archive) repository
------------------------------------------------
Adding PPA on Ubuntu

	$ sudo -s
	# add-apt-repository ppa:resmo/git-ftp
	# aptitude update
	# aptitude install git-ftp

Note: Usually updated after every release (tag).


Mac OS X
--------
Using homebrew:

	$ brew install git-ftp


Windows
-------
There are at least two ways to install git-ftp on Windows.

 * Using cygwin only
 * Using cygwin and msysgit (recommended)

First install cygwin and install the package 'curl'.
If you like to use cygwin only, install package 'git',
otherwise install msysgit.

After this, open git bash (or cygwin bash for cygwin only):

	$ cd ~
	$ git clone http://github.com/resmo/git-ftp git-ftp.git
	$ cd git-ftp.git && chmod +x git-ftp
	$ cd /bin/
	$ ln -s ~/git-ftp.git/git-ftp git-ftp

Note: Option -p without argument is showing password while entering.


Upstream using symlinking
-------------------------

This usually works on Linux based systems, but not on Mac OS X without extending $PATH.

Note: Make sure Git and cURL is installed.

This is a easy way to have more then one git-ftp installed

	$ mkdir -p ~/develop/git-ftp.git
	$ cd ~/develop/git-ftp.git
	$ git clone http://github.com/resmo/git-ftp.git .
	$ chmod +x git-ftp
	$ mkdir ~/bin && cd ~/bin/
	$ ln -s ~/develop/git-ftp.git/git-ftp git-ftp.dev

After this you can use 'git ftp.dev' or 'git-ftp.dev'

Update to the latest version is simple as:

	$ cd ~/develop/git-ftp.git
	$ git pull
