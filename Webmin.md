# Webmin

    [download <webmin>.deb]
    sudo apt-get openssl install perl libnet-ssleay-perl libauthen-pam-perl libpam-runtime libio-pty-perl apt-show-versions python
    sudo dpkg -i <webmin>.deb
    [add 'webmin' file] /etc/ufw/applications.d/webmin
    [[
        [Webmin]
        title=Webmin
        description=Webmin
        ports=<port>/tcp
    ]]
    sudo ufw allow Webmin
    sudo ufw allow Webmin from <port>
