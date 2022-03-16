# Advance Commands

## Table of Contents

| [`crontab`](#crontab) |

-----

## crontab
>
* entry point to work with cron jobs.
* Cron jobs are jobs that are scheduled to run at specific intervals. You might have a command perform something every hour, or every day, or every 2 weeks Or on weekends.
[`crontabgen`](#https://crontab-generator.org/)

    Ex:
        $> crontab -l - which cron jobs are defined by you
        $> crontab -e - to edit the cron jobs, and add new ones, this opens with the default editor
        $> EDITOR=nano crontab -e - to edit in nano editor
