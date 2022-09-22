# chartjs-test

# Error: ENOSPC: System limit for number of file watchers reached
echo fs.inotify.max_user_watches=524288 | sudo tee -a /etc/sysctl.conf && sudo sysctl -p # that modifies the file watch limit to max 524,288 which consume approx. 512MB Ram for 64bit. # reduce that number to consume less memory. # to see if that did it run cat /proc/sys/fs/inotify/max_user_watches # you should see fs.inotify.max_user_watches=524288
