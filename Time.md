# Time

    sudo dpkg-reconfigure tzdata
    sudo ntpdate ntp.ubuntu.com
    sudo apt-get install ntp
    sudo ntpq -p
    [ntp config file] /etc/ntp.conf
    [on config change] sudo service ntp restart
