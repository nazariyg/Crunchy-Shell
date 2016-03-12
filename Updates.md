# Updates

    ([comment out 'deb...' for Universe and Multiverse repos] /etc/apt/sources.list)
    sudo apt-get update
    sudo apt-get upgrade
    sudo aptitude safe-upgrade
    sudo apt-get autoremove
    [select 'Yes'] sudo dpkg-reconfigure -plow unattended-upgrades
    [configure email settings, blacklist etc.] /etc/apt/apt.conf.d/50unattended-upgrades
    [dpkg log file] /var/log/dpkg.log
    [unattended-upgrades log file] /var/log/unattended-upgrades
    sudo apt-get install -f
    [list installed packages] dpkg --get-selections
    [show package dependencies] apt-cache showpkg <packagename>
    [show package dependencies] apt-cache depends <packagename>
    [show reverse package dependencies] apt-cache rdepends <packagename>
