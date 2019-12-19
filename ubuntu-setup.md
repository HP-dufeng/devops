# ubuntu server 

## hostname
```
hostnamectl set-hostname console.feng.com
```

## set root password
```
sudo passwd root
```

## ssh
```
/etc/ssh/sshd_config
    PermitRootLogin yes
```
```
sudo service ssh restart
```

## static ip
/etc/netplan/50-cloud-init.yaml
```
network:
    ethernets:
        eth0:
            dhcp4: no
            addresses: [192.168.1.10/24]
            gateway4: 192.168.1.1
            nameservers:
                    addresses: [192.168.1.1]
    version: 2
    renderer: networkd
```
```
sudo netplan apply
systemd-resolve --status
```