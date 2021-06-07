If using python/perl/bash etc. script to run a process behind CGI, 
Remember that when cgi url is hit, the cgi script is not run as root user.
It is probably run as `www-data user`
Check the list of users by: `cut -d: -f1 /etc/passwd`

so you need to ensure correct persmissions are present on the file to be run behind cgi.

rwxr-xr-x is what is ideally used.
**7 5 5**

**First rwx: User**
A user is the owner of the file. By default, the person who created a file becomes its owner. Hence, a user is also sometimes called an owner.

**Second r-x: Group**
A user- group can contain multiple users. All users belonging to a group will have the same Linux group permissions access to the file. Suppose you have a project where a number of people require access to a file. Instead of manually assigning permissions to each user, you could add all users to a group, and assign group permission to file such that only this group members and no one else can read or modify the files.

**Third r-x: Other**
Any other user who has access to a file. This person has neither created the file, nor he belongs to a usergroup who could own the file. 
