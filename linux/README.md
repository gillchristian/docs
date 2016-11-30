
# Linux and all terminal things

## Content

1. [Processes](#processes)
  1. [List processes by port](#list-processes-by-port)
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

## Remote

### SSH

#### Add SSH Key to DigitalOcean droplet

[Article](https://www.digitalocean.com/community/tutorials/how-to-use-ssh-keys-with-digitalocean-droplets).
