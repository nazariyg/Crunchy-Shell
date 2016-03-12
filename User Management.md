# User Management

    sudo adduser <username> sudo
    sudo adduser root www-data
    sudo adduser <username> www-data
    [become root] sudo su
    [create root account] sudo passwd
    [delete root account] sudo passwd -l root
    ['DIR_MODE 0700'] /etc/adduser.conf
    [user home directory template] /etc/skel
    [password ... sha... min=<minpasslen>] /etc/pam.d/common-password
    [user config file] /etc/passwd
    [group config file] /etc/group
    [sudoers config file] (/etc/sudoers) sudo visudo
    sudo chage -l <username>
    id -gn <username>
    sudo passwd <username>
    sudo adduser <username>
    sudo deluser <username>
    sudo addgroup <groupname>
    sudo delgroup <groupname>
    sudo adduser <username> <groupname>
    sudo adduser <username> sudo
    sudo deluser <username> <groupname>
    sudo passwd -l <username>
    sudo passwd -u <username>
    sudo getent group <groupname>
