This level is similar to the previous two. The catch here is that you actually have to write a shell script. Don't worry it's not something complicated. All you have to do is read a file and redirect the contents of that file to a location where is is accessible by all users.

There are two symbols of note in this particular exercise > and >>

">" redirects output to a file, overwriting the file

">>" redirects output to a file appending(adding) the redirected output at the end of the file

Either of them can do for this task.

The file we have to read is bandit24 located in /etc/bandit_pass. It can only be read by user bandit24.

Following the steps in the previous 2 exercises leads you to the file cronjob_bandit24.sh

Reading the file you see that it is executing a shell script to delete everything in the directory /var/spool/$myname

$myname is the user running the script. So to execute a command as a user, simply copy whatever script to a directory under /var/spool/ named similarly to the user. In this case the user is bandit24.

NOTE: You have no read and write access to the /var/spool/bandit24 directory. So you have to create the script elsewhere and copy it there and redirect the contents of the file to a directory in which you have read access. A shell script is started by specifying which shell is going to execute it.

ALSO NOTE: You have to ensure that the script you write is executable by all users, and that the directory is writable by all users. Simply give everyone permissions to read, write and execute.




Command: cd /tmp/
         mkdir -v <directory name>
         chmod -v 777 <directory name>
         cd <directory name>
         vim <shell script>
         chmod -v 777 <shell script>
         cp -v <shell script> /var/spool/bandit24/

chmod changes the permissions to files and folders. Refererence https://wiki.archlinux.org/index.php/File_permissions_and_attributes#Changing_permissions

You'll have to wait for a minute before anything happens. This is because the cron job runs every minute.




password for level 24: UoMYTrfrBFHyQXmg6gzctqAwOmw1IohZ
