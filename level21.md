In this level we are introduced to cron jobs.

Cron is unix's task scheduler. If you want something done at a certain time on a certain day in a certain month, then cron is for you.

We're supposed to go into /etc/cron.d/ and see what files are running.

There are a number of files in the directory but our immediate task is getting to level 22. So we focus on the one written cronjob_bandit22

On opening the file we find this 
    "* * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null"

What the 5 stars mean is that for every minute of every hour of every day of the month of every month of every day of the week run whatever comes next

The first 5 values of cron are ordered as follows starting from the far left
    minute (0-59) 0 being the 60th minute
    hour (0-23) 0 being midnight
    month (1-12)
    day of week (0-6) 0 being Sunday

After the first 5 stars what comes next should be run as user bandit22. That's what bandit22 stands for

So as bandit22 run the shellscript cronjob_bandit22.sh located in /usr/bin/ and direct that output to /dev/null. &> is and direct to. /dev/null is the black hole where you throw everything you never want to see again




Commands: cd /etc/cron.d
          cat cronjob_bandit22
          cd
          cd /usr/bin
          cat cronjob_bandit22.sh
          cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv




password to level 22: Yk7owGAcWjwMVRwrTesJEwB7WVOiILLI
