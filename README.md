# Logrotate
logrotate is intended to make system management easier for systems that create a large number of log files.
It supports automated log file rotation, compression, removal, and mailing.
Each log file may be handled on a daily, weekly, or monthly basis, or if it becomes too large. 

Normally, logrotate is run as a daily cron job. 

<br>

## **Table of Contents**
* [Home](https://github.com/Ahhhh-man/logrotate-template/wiki/Home)
* [Installation](https://github.com/Ahhhh-man/logrotate-template/wiki/Installation)
    * [Debian and Ubuntu](https://github.com/Ahhhh-man/logrotate-template/wiki/Installation#on-debian-and-ubuntu)
    * [CentOS, RHEL and Fedora](https://github.com/Ahhhh-man/logrotate-template/wiki/Installation#on-centos-rhel-and-fedora)
* [Directives](https://github.com/Ahhhh-man/logrotate-template/wiki/Directives)
* [Examples](#examples)
* [Further Reading](#further-reading)

<br>

## **Examples**

Daily rotation of the log file /var/log/messages with 7 days retention:

```
/var/logs/example/example.log {
    rotate 7
    daily
    missingok
    ifempty
    maxage 7
    compress
    delaycompress
    dateext
    dateformat -%Y%m%d
    extension .log
}
```

<br>

## **Further Reading**

* https://github.com/logrotate/logrotate
* https://www.digitalocean.com/community/tutorials/how-to-manage-logfiles-with-logrotate-on-ubuntu-16-04
