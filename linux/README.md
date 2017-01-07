
# Linux and all terminal things

## Content

1. [Vim](https://github.com/gillchristian/docs/tree/master/linux/vim).
1. [zsh](https://github.com/gillchristian/docs/tree/master/linux/zsh).
1. [Processes](#processes)
  1. [List processes by port](#list-processes-by-port)
1. [Services](#services)
  1. [Systemctl](#systemctl)
1. [Remote](#remote)
  1. [SSH](#ssh)
    1. [Add SSH Key to DigitalOcean droplet](#add-ss-hey-to-digitalocean-droplet)

## Processes

### List processes by port

```bash
$ netstat -tulpn
```

Example output

```bash
Active Internet connections (only servers)
Proto Recv-Q Send-Q Local Address           Foreign Address         State       PID/Program name
tcp        0      0 127.0.0.1:3000          0.0.0.0:*               LISTEN      18042/ruby
tcp        0      0 127.0.0.1:5432          0.0.0.0:*               LISTEN      1046/postgres
tcp6       0      0 :::9838                 :::*                    LISTEN      22066/node
tcp6       0      0 :::9200                 :::*                    LISTEN      18624/java
udp6       0      0 :::54328                :::*                                18624/java
udp6       0      0 :::5353                 :::*                                2713/google-chrome-
udp6       0      0 :::56325                :::*                                796/avahi-daemon: r
```

Use `grep` to find specif ones

```bash
$ netstat -tulpn | grep :80
```

#Services

###Systemctl

`Systemd` is an init system and system manager that is widely becoming the new standard for Linux machines.

####Start, stop, restart, reload, enable, disable & status

```bash
$ sudo systemctl start application.service
# or
$ sudo systemctl start application

$ sudo systemctl stop application

$ sudo systemctl restart application

$ sudo systemctl reload application

$ sudo systemctl reload-or-restart application

$ sudo systemctl enable application

$ sudo systemctl disable application

$ sudo systemctl status application
```

`reload` is used to initiate the processes of an application that is able to reload the configuration files (without restarting).

`enable` will create a symbolic link from the system's copy of the service file into the location on disk where `systemd` looks for autostart files.

####Add services

[CoreOS's Article](https://coreos.com/docs/launching-containers/launching/getting-started-with-systemd/)

## Remote

### SSH

#### Add SSH Key to DigitalOcean droplet

[Article](https://www.digitalocean.com/community/tutorials/how-to-use-ssh-keys-with-digitalocean-droplets).
