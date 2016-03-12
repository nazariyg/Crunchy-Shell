# Network

## Installs

    sudo apt-get install ethtool
    sudo apt-get install traceroute

## Commands

    ifconfig -a
    ifconfig eth0
    sudo lshw -class network
    sudo ethtool eth0
    ip addr list
    route
    route -n
    sudo netstat
    sudo netstat -s
    sudo netstat -at
    sudo netstat -atn
    sudo netstat -tulpn
    sudo dhclient
    ping <host>
    tracepath <host>
    sudo traceroute <host>
    dig <host>
    dig <host> +short
    dig <host> +trace

## Config Files

    /etc/network/interfaces
    [[
        auto eth0
          iface eth0 inet static
          address 192.168.0.102
          netmask 255.255.255.0
          gateway 192.168.0.1
          network 192.168.0.0
          broadcast 192.168.0.255
          dns-nameservers 192.168.0.1
    ]]
    /etc/hosts
    /etc/nsswitch.conf
    (/etc/host.conf)
    (/etc/resolv.conf)
    (/etc/resolvconf/resolv.conf.d/base)

## Restarting & On/Off

    sudo /etc/init.d/networking <verb>
    sudo service networking <verb>
    sudo ifup eth0
    sudo ifdown eth0
    ifconfig eth0 <verb>
