# Monitoring

## General

    top
    ps -ef
    ps -aux
    free
    file <filename>
    sudo apt-get install linux-crashdump
    cat /proc/cmdline
    dmesg | grep -i crash
    dmesg | tail

## sysstat

    sudo apt-get install sysstat
    sudo dpkg-reconfigure sysstat
    sar
    sar -r
    sar -b
    [log files] /var/log/sysstat
