# SSL

    sudo apt-get install openssl libssl-dev
    sudo openssl genrsa -out server.key 2048
    sudo openssl req -new -key server.key -out server.csr
    (sudo cp server.key server.key.orig)
    (sudo openssl rsa -in server.key.orig -out server.key)
    sudo openssl x509 -req -days 796 -in server.csr -signkey server.key -out server.crt
    sudo chmod 600 server.key
    [add 'openssl' file] /etc/ufw/applications.d/openssl
    [[
        [OpenSSL]
        title=OpenSSL
        description=OpenSSL
        ports=443/tcp
    ]]
    sudo ufw allow OpenSSL
    sudo ufw allow OpenSSL from <port>
    sudo openssl engine -t

## Converting .pub and RSA keys to PEM

    ssh-keygen -f <srcpubfile> -e -m pem > <dstpemfile>
    openssl rsa -in <srcrsafile> -outform pem > <dstpemfile>
