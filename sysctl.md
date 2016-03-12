# sysctl

    [make sure that everything is commented out in] /etc/sysctl.conf
    [get sysctl-add.conf]
    sudo sh -c 'cat sysctl-add.conf >> /etc/sysctl.conf'
    sudo sysctl -p
    ([reboot])
