Linux System Administrator/DevOp Interview Questions
====================================================

A collection of linux sysadmin/devop interview questions. Feel free to contribute via pull requests, issues or email messages.


## <a name='toc'>Table of Contents</a>

  1. [Contributors](#contributors)
  1. [General Questions](#general)
  1. [Simple Linux Questions](#simple)
  1. [Medium Linux Questions](#medium)
  1. [Hard Linux Questions](#hard)
  1. [Expert Linux Questions](#expert)
  1. [Networking Questions](#network)
  1. [DevOp Questions](#devop)
  1. [Fun Questions](#fun)
  1. [Demo Time](#demo)
  1. [Other Great References](#references)


####[[⬆]](#toc) <a name='contributors'>Contributors:</a>

* [moregeek](https://github.com/moregeek)
* [typhonius](https://github.com/typhonius)
* martin
* [negesti](https://github.com/negesti)
* peter
* [andreashappe](https://github.com/andreashappe)
* [quatrix](https://github.com/quatrix)
* [biyanisuraj](https://github.com/biyanisuraj)

The majority of the questions were collected from:

* https://github.com/gurmeet1109/docgurmeet/tree/master/InterviewQuestionsSamples
* https://github.com/kylejohnson/linux-sysadmin-interview-questions/blob/master/test.md


####[[⬆]](#toc) <a name='general'>General Questions:</a>

* What did you learn yesterday/this week?
* Talk about your preferred development/administration environment. (OS, Editor, Browsers, Tools etc.)
* Tell me about the last major Linux project you finished.
* Tell me about the biggest mistake you've made in [some recent time period] and how you would do it differently today. What did you learn from this experience?
* What function does DNS play on a network?
  Mappings of addresses to names and vice versa (known as records) are stored in a database
* What is HTTP?
  HyperText Transfer Protocol (HTTP) is the underlying protocol used by the World Wide Web to define how messages  are formatted and transmitted. 
* What is an HTTP proxy and how does it work?
  A HTTP proxy speaks the HTTP protocol, it's especially made for HTTP connections but can be abused for other protocols as well
* What is SMTP? Give the basic scenario of how a mail message is delivered via SMTP!
  Simple Mail Transfer Protocol (SMTP) is an Internet standard for electronic mail (e-mail) transmission.
* What is RAID? What is RAID0, RAID1, RAID5, RAID10?
  RAID(redundant array of independent disks).
  RAID0: Blocks striped, no mirror. no parity. 
  RAID1: Blocks mirrored, no stripe. no parity. 
  RAID5: min 3 disks. blocks striped, distributed parity.
  RAID10: min 4 disks, blocks mirrored. 
* What is a level 0 backup? What is an incremental backup?
  level 0: full backup. 
  Incremental: identifying, recording and, thus, preserving only those files that have changed since the last 
  backup. 
* Describe the general file system hierarchy of a Linux system.
  central concepts are superblock, inode, data block, directory block, and indirection block.Linux chooses to have   a single hierarchical directory structure. Everything starts from the root directory, represented by /, and then expands into sub-directories instead of having so-called 'drives'. 
       /bin       Essential command binaries
       /boot      Static files of the boot loader
       /dev       Device files
       /etc       Host-specific system configuration
       /lib       Essential shared libraries and kernel modules
       /media     Mount point for removeable media
       /mnt       Mount point for mounting a filesystem temporarily
       /opt       Add-on application software packages
       /sbin      Essential system binaries
       /srv       Data for services provided by this system
       /tmp       Temporary files
       /usr       Secondary hierarchy
       /var       Variable data


####[[⬆]](#toc) <a name='simple'>Simple Linux Questions:</a>

* What is the name and the UID of the administrator user?
  Root, UID: 0. 
* How to list all files, including hidden one, in a directory?
  ls -a
* What is the Unix/Linux command to remove a directory and its contents?
  rm -rf directoryname
* Which command will show you free/used memory? Does free memory exist on Linux?
  free
* How to search for the string "my konfi is the best" in files of a directory recursively?
  cd /path/to/dir
  find . -type f -exec grep -l "word" {} +
* How to connect to a remote server or what is SSH?
* How to get all environment variables and how can you use them?
  printenv
* I get "command not found" for ```ifconfig -a```. What can be wrong?
  as root? 
* What happens if I type TAB-TAB?
  display all methods
* What command will show the available disk space on the Unix/Linux system?
  df -h #human readable
* What command is used to lookup DNS records?
  dig
* What Unix/Linux commands will alter a files ownership, files permissions?
  chown, chmod
* What does ```chmod +x FILENAME```do?
  exe
* What does the permission 0750 on a file mean?
Owner may read, write and execute. The Group may read and execute. (but not write) The world may not do anything with this file.
  0750 = User:rwx Group:r-x World:---
* What does the permission 0750 on a directory mean?
  0755 (drwxr-xr-x)
* How to add a new system user without login permissions?
* How to add/remove a group from a user?
  deluser user group
* What is a bash alias?
  A Bash alias is essentially nothing more than a keyboard shortcut, an abbreviation, a means of avoiding typing a long command sequence. If, for example, we include alias lm="ls -l. more" in the ~/.bashrc file, then each lm typed at the command-line will automatically be replaced by a ls -l.

* How do you set the mail address of the root/a user?
  /etc/alias
* What does CTRL-c do?
* What is in /etc/services?
* How to redirect STDOUT and STDERR in bash? (> /dev/null 2>&1)
* What is the difference between UNIX and Linux
* What is the difference between Telnet and SSH?
* Explain the three load averages and what do they indicate
  Load average is a gauge of how many processes are on average, concurrently demanding CPU attention.
  the load average of the system over the last 1, 5, and 15 minutes.


####[[⬆]](#toc) <a name='medium'>Medium Linux Questions:</a>

* What do the following commands do?
 * ```tee```
   Tee command is used to store and view (both at the same time) the output of any other command.
 * ```awk```
   Awk is both a programming language and text processor that can be used to manipulate text data in very useful ways.
 * ```tr```
  tr abbreviated as translate or transliterate. It takes as parameters two sets of characters, and replaces occurrences of the characters in the first set with the corresponding elements from the other set i.e. it is used to translate characters.
 * ```cut```
  cut is used for text processing
 * ```tac```
    Concatenate and print files in reverse.
 * ```curl```
   transfer a URL
 * ```wget```
wget stands for "web get". It is a command-line utility which downloads files over a network.
 * ```watch```
     execute a program periodically, showing output fullscreen
 * ```tail```
* What does a ```&``` after a command do?
  makes the command run in the background. 
* What does ```& disown``` after a command do?
* What is a packet filter and how does it work?
* What is swap and what is it used for?
* What is an A record, an NS record, a PTR record, a CNAME record, an MX record?
 * Are there any other RRs and what are they used for?
* What is the sticky bit?
* What is the difference between hardlinks and symlinks? What happens when you remove the source to a symlink/hardlink?
* What is an inode and what fields are stored in an inode?
* Howto force/trigger a file system check on next reboot?
* What is SNMP and what is it used for?
* What is a runlevel and how to get the current runlevel?
* What is SSH port forwarding?
* What is the difference between local and remote port forwarding?
* What steps to add a user to a system without using useradd/adduser?
* What is MAJOR and MINOR numbers of special files?
* Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.
* Describe a scenario when deleting a file, but 'df' not showing the space being freed.
* Describe how 'ps' works.
* What happens to a child process that dies and has no parent process to wait for it and what’s bad about this?
* How to know which process listens on a specific port?


####[[⬆]](#toc) <a name='hard'>Hard Linux Questions:</a>

* What is the difference between processes and threads?
* What is a tunnel and how you can bypass a http proxy?
* What is the difference between IDS and IPS?
* What shortcuts do you use on a regular basis?
* What is the Linux Standard Base?
* What is an atomic operation?
* Your freshly configured http server is not running after a restart, what can you do?
* What kind of keys are in ~/.ssh/authorized_keys and what it is this file used for?
* I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?
* Did you ever create RPM's, DEB's or solaris pkg's?
* What does ```:(){ :|:& };:``` do on your system and why you would care about that?
* How trace system call and signal?
* What's happening when the Linux kernel is starting the OOM killer, how does it choose which process to kill first.
* Describe the linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.
* What's a chroot jail?
* When trying to umount a directory it says it's busy, how to find out which PID holds the directory?
* What's LD_PRELOAD and when it's used?
* You run a binary and nothing happens, how do you debug what's doing?


####[[⬆]](#toc) <a name='expert'>Expert Linux Questions:</a>

* A running process gets ```EAGAIN: Resource temporarily unavailable``` on reading a socket. How you can close this bad socket/file descriptor without killing the process?


####[[⬆]](#toc) <a name='network'>Networking Questions:</a>

* What is localhost and why would ```ping localhost``` fail?
* What is the similarity between "ping" & "traceroute" ? How is traceroute able to find the hops.
* What command is used to show all open ports and/or socket connections on a machine?
* Is 300.168.0.123 a valid IPv4 address?
* Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?
* What is a VLAN?
* What is ARP and what is it used for?
* What is the difference between TCP and UDP?
* What is the purpose of a default gateway?
* What command is used to show the route table for a machine?
* A TCP connection on a network can be uniquely defined by 4 things. What are those things?
* When a client running a web browser connects to a web server, what is the source port and what is the destination port of the connection?
* How do you add an IPv6 address to a specific interface?
* You have added an IPv4 and IPv6 address to interface eth0. A ping to the v4 address is working but a ping to the v6 address gives yout the response ```sendmsg: operation not permitted```. What could be wrong?


####[[⬆]](#toc) <a name='devop'>DevOp Questions:</a>

* Can you describe your workflow when you create a script?
* What is GIT?
* What is a dynamically/statically linked file?
* What does "configure && make && make install"?
* What is puppet/chef/ansible used for?
* How do you create a new mysql user?
* How do you create a new postgres user?
* What is a virtual IP address? What is a cluster?
* How print the strings of printable characters in files?
* How look shared library dependencies?
* What is Automake and Autoconf?
* ./configure shows an error that libfoobar is missing on your system, how could you fix this, what could be wrong?
* Advantages/disadvantages of script vs compiled program.
* What is the difference between fork and thread? And parent and child process in fork system call?
* What's the relationship between continuous delivery and DevOps?
* What are the important aspects of a system of continous integration and deployment?


####[[⬆]](#toc) <a name='fun'>Fun Questions:</a>

* A careless sysadmin executes the following command: ```chmod 444 /bin/chmod ``` - what do you do to fix this?
* I've lost my root password, what can I do?
* I've rebooted a remote server but after 10 minutes I'm still not able to ssh into it, what can be wrong?
* If you were stuck on a desert island with only 5 command-line utilities, which would you choose?
* You come across a random computer and it appears to be a command console for the universe. What is the first thing you type?
* Tell me about a creative way that you've used SSH?


####[[⬆]](#toc) <a name='demo'>Demo Time:</a>

* Unpack test.tar.gz without man pages or google.
* Remove all "*.pyc" files from testdir recursively?
* Search for "my konfu is the best" in all *.py files.
* Replace the occurrence of "my konfu is the best" with "I'm a linux jedi master" in all *.txt files.
* :interrobang: more on files ... cut, tr, awk ...
* Test if port 443 on a machine with IP address X.X.X.X is reachable.
* Get http://myinternal.webserver.local/test.html via telnet.
* How to send an email without a mail client, just on the command line?
* Write a ```get_prim``` method in python/perl/bash/pseudo.
* Find all files which have been accessed within the last 30 days.
* Explain the following command ```(date ; ps -ef | awk ‘{print $1}’ | sort | uniq | wc -l ) >> Activity.log```
* Write a script to list all the differences between two directories.
* Write a program in any language you choose, to reverse a file.
* In a log file with contents as ```<TIME> : [MESSAGE] : [ERROR_NO] - Human readable text``` display summary/count of specific error numbers that occured every hour or a specific hour


####[[⬆]](#toc) <a name='references'>Other Great References:</a>

Some questions are 'borrowed' from other great references like:

* https://github.com/darcyclarke/Front-end-Developer-Interview-Questions
* https://github.com/kylejohnson/linux-sysadmin-interview-questions/blob/master/test.md
* https://github.com/gurmeet1109/docgurmeet/tree/master/InterviewQuestionsSamples
* http://slideshare.net/kavyasri790693/linux-admin-interview-questions
