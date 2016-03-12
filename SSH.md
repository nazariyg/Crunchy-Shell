# SSH

    (sudo apt-get install openssh-server)

## SSH Keys

    ssh-keygen -t rsa
    cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
    [copy the private key to the login-from hosts]

    sudo -i
    cd ~
    ssh-keygen -t rsa
    cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
    [copy the private key to the login-from host(s)]
    [create root account] sudo passwd
    ([reconnect])

## Configuration

    sudo addgroup sshg
    sudo adduser root sshg
    sudo adduser <username> sshg
    sudo cp -p /etc/ssh/sshd_config /etc/ssh/sshd_config.orig
    sudo chmod 600 /etc/ssh/sshd_config
    sudo chmod 600 /etc/ssh/sshd_config.orig

    ['PasswordAuthentication no'] /etc/ssh/sshd_config
    ['Port <port>'] /etc/ssh/sshd_config
    [repeat SSH port] /etc/ufw/applications.d/openssh-server
    sudo ufw allow OpenSSH
    ['LogLevel VERBOSE']                   /etc/ssh/sshd_config
    (['PermitRootLogin no']                /etc/ssh/sshd_config)
    ['RSAAuthentication yes']              /etc/ssh/sshd_config
    ['PubkeyAuthentication yes']           /etc/ssh/sshd_config
    ['PermitEmptyPasswords no']            /etc/ssh/sshd_config
    ['ChallengeResponseAuthentication no'] /etc/ssh/sshd_config
    ['UsePAM no']                          /etc/ssh/sshd_config
    ([add 'DenyUsers root']                /etc/ssh/sshd_config)
    [add 'AllowGroups sshg']               /etc/ssh/sshd_config
    ([add 'ClientAliveInterval 120']       /etc/ssh/sshd_config)

    sudo chmod 600 /var/log/auth.log
    [on config change] sudo service ssh restart
    [log file] /var/log/auth.log

## Connecting

    ssh -i <key> -p <port> <username>@<host>
    ssh -t <username>@<host> "/bin/bash"
