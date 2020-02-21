# rc.uwsgi

Copyright 2019, 2020 Vid Podpečan



## How to use

This script can be used for basic control of uWSGI in emperor mode on Slackware Linux. Please note that you need uWSGI >= 1.9.17 which supports master FIFO. The script was tested on Slackware 14.2 but should work on every not too ancient Linux.

On Slackware, copy this script into `/etc/rc.d/` and give it proper permissions, e.g.:

```
chown root:root /etc/rc.d/rc.uwsgi
chmod 755 /etc/rc.d/rc.uwsgi
```



The following parameters should be modified to suit your own configuration:

-   location of uwsgi binary (default: `/usr/bin/uwsgi`)
-   vassals directory (default: `/etc/uwsgi/vassals`)
-   user (default: `www-data`)
-   group (default: `www-data`)
-   master FIFO file (default: `/tmp/uwsgi.fifo`)
-   emperor PID file (default: `/tmp/uwsgi-emperor.pid`)
-   log file (default: `/var/log/uwsgi-emperor.log`)
