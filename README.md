# ubuntu24.04-settings
## crontab configuration
  For start-up applications, crontab job @reboot is used. Apparmor needs to be disabled for Docker Desktop startup
  Sanp application does not seem to start with Cron job nor Startup application????

```bash
#!/bin/bash

# Start AdGuard Home
/usr/bin/snap start adguard-home
sysctl -w kernel.apparmor_restrict_unprivileged_userns=0
systemctl --user restart docker-desktop\
```
