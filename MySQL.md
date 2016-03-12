# MySQL

## General

    sudo apt-get install mysql-server
    (sudo dpkg-reconfigure mysql-server-5.5)
    /etc/mysql/my.cnf
    [add to '[mysqld]' section in] /etc/mysql/my.cnf
    [[
        (interactive_timeout = 60)
        (wait_timeout = 60)
        default-time-zone = +00:00
    ]]
    mysql -u root -p
    grant all on `<database>`.* to '<user>'@'localhost' identified by '<password>';
    select `user`, `host` from `mysql`.`user`;
    [check time zone settings] select @@global.time_zone;

## Maintenance

    sudo service mysql restart
    sudo service mysql stop
    sudo service mysql start
    [check a database] mysqlcheck -u root -p<password> --all-databases
    [backup a database: gz] mysqldump -u root -p<password> --add-drop-database --databases <database> | gzip -9 > <dstfile>.sql.gz
    [backup a database: 7z] mysqldump -u root -p<password> --add-drop-database --databases <database> | 7z a -mx=9 -si <dstfile>.sql.7z
    [restore a database: gz] gunzip < <srcfile>.sql.gz | mysql -u root -p<password>
    [restore a database: 7z] 7z e -so <srcfile>.sql.7z | mysql -u root -p<password>
