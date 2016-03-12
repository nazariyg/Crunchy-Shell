# FTP

    sudo apt-get install vsftpd
    sudo adduser ftpuser
    (sudo apt-get install ssl-cert)
    (sudo make-ssl-cert generate-default-snakeoil --force-overwrite)

## Configuration

    ['listen_port=8586']                     /etc/vsftpd.conf
    ['anonymous_enable=NO']                  /etc/vsftpd.conf
    ['local_enable=YES']                     /etc/vsftpd.conf
    ['write_enable=YES']                     /etc/vsftpd.conf
    ['ssl_enable=YES']                       /etc/vsftpd.conf
    ['rsa_cert_file=<cert.pem>']             /etc/vsftpd.conf
    ['rsa_private_key_file=<private.key>']   /etc/vsftpd.conf
    (['require_ssl_reuse=NO']                /etc/vsftpd.conf)
    (['force_local_logins_ssl=YES']          /etc/vsftpd.conf)
    ['pasv_min_port=21000']                  /etc/vsftpd.conf
    ['pasv_max_port=21021']                  /etc/vsftpd.conf
    ['userlist_enable=YES']                  /etc/vsftpd.conf
    ['userlist_deny=NO']                     /etc/vsftpd.conf
    ['userlist_file=/etc/vsftpd.user_list']  /etc/vsftpd.conf
    ['text_userdb_names=YES']                /etc/vsftpd.conf
    ['ftpuser'] /etc/vsftpd.user_list
    [on config change] sudo /etc/init.d/vsftpd restart
    [add 'ftp' file] /etc/ufw/applications.d/ftp
    [[
        [Ftp]
        title=Ftp
        description=Ftp
        ports=8586,21000:21021/tcp
    ]]
    sudo ufw allow Ftp
