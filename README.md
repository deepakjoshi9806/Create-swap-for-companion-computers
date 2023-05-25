#### Create-swap-for-companion-computers
- `sudo fallocate -l 10G /home/swapfile`
- `sudo chmod 600 /home/swapfile`
- `sudo mkswap /home/swapfile`
- `sudo swapon /home/swapfile`
- Make sure its set up correctly
- `sudo swapon --show`
- make it permanent
` sudo echo "/home/swapfile none swap sw 0 0" >> /etc/fstab`
- Edit your  /etc/sysctl.conf and add
`vm.swappiness=10`
- reboot the system
- check virtual memory size (swap size should be shown if everything was setup correctly)
`cat /proc/meminfo`
