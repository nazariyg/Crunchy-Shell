# Firewall

    sudo ufw default deny
    sudo ufw allow OpenSSH
    sudo ufw enable
    sudo ufw app list
    sudo ufw app info <appname>
    /etc/ufw/applications.d
    sudo ufw allow <appname>
    sudo ufw status
    sudo ufw status verbose
    sudo ufw status numbered
    sudo ufw allow <port>
    sudo ufw <verb> from <ip/cidr> to any port <port>
    sudo ufw delete <rule>
    sudo ufw --dry-run <rule>
    /etc/services
    sudo ufw logging on
