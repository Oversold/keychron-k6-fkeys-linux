# keychron-k6-fkeys-linux


STEP 1

sudo nano /etc/systemd/system/keychron.service


STEP 2

input the following

[Unit]
Description=The command to make the Keychron K2 work

[Service]
Type=oneshot
ExecStart=/bin/bash -c "echo 0 > /sys/module/hid_apple/parameters/fnmode"

[Install]
WantedBy=multi-user.target

then save/exit

STEP 3

in terminal
  systemctl enable keychron
  
STEP 4

REBOOOOOT
