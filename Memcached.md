# Memcached

    sudo apt-get install memcached
    [config file] /etc/memcached.conf
    [add 'memcached' file] /etc/ufw/applications.d/memcached
    [[
        [Memcached]
        title=Memcached
        description=Memcached
        ports=11211/tcp
    ]]
    sudo ufw allow Memcached
