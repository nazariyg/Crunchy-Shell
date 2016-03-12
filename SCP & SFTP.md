# SCP & SFTP

    scp -i <key> -P <port> <username>@<host>:<remotesrc> <localdst>
    scp -i <key> -P <port> <localsrc> <username>@<host>:<remotedst>
    sftp -i <key> -P <port> <username>@<host>
