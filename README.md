# Automate
To wake up the system every day at specific time and execute a script:
Pre-requisite: System needs to be powered on all the time. It can go to sleep to save energy consumption.
Steps: Applicable to Mac 

1.	Log in as super user (root)—in terminal, >sudo su and give root password
2.	Cmd to set a schedule to wake up the system: pmset repeat wake MTWRFSU 5:55:00
3.	A cron job (can be run by any user of the system) is required to run a job at specific time.
a.	From terminal : crontab -e : this lists the existing cron jobs. Edit this file so that the chosen script runs at specified time. Each command on its own line.
Eg: 
00 06 * * * /Users/john/opt/anaconda3/bin/python3 /Users/john/Documents/GitHub/tiny_python_projects/sankarasTest/newsapi_us_hyperlink.py
05 06 * * * /Users/john/opt/anaconda3/bin/python3 /Users/john/Documents/GitHub/tiny_python_projects/sankarasTest/newsapi_India_hyperlink.py

Ref:
1.pmset : manipulate power management settings 
2: https://www.macworld.com/article/621076/how-to-schedule-your-mac-to-turn-off-and-on.html
