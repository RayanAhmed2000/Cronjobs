# What is Cron-job
- Cron is the most useful utility in a Linux or UNIX-like operating system that allows running commands or scripts on a given schedule without any user intervention.
- The scheduled commands and scripts are also named as cron jobs.

# What is crond
- Crond is the daemon in the Linux system that runs in the background and checks every minute to see if there is any job scheduled at that time. If there is, it performs that job, else it remains inactive.

# Syntax of cronjob
- ***** (msdmw) command/script
- crontab file location
```
cat /etc/crontab
```
- user specific cronjobs are located in
```
cd /var/spool/cron/crontabs
```
# creating a cronjob file
- A standard user can define a cron job using the following command:
```
crontab -e
```
- To edit the crontab file for any other user
```
sudo crontab -u <username> -e
```
# Tutorial 
- Run a cron job every 15 minutes
```
*/15 * * * * command/script
```
- Run a cron job at 5 am every day
```
0 5 * * * command/script
```
- Run a cron job at 5 pm every day
```
0 17 * * * command/script
```
- Run a cron job at 9 am on the first day of every month
```
0 9 1 * * command/script
```
- Run a cron job every 5 hours
```
0 */5 * * * command/script
```

