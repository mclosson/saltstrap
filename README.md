# saltstrap
Bootstrap Saltstack onto various operating systems and hosting environments

## Example SSH configuration

```sh
$ cat ~/.ssh/config
Host salt
HostName 10.9.8.7
Port 22
User freebsd
ServerAliveInterval 120
IdentityFile ~/.ssh/id_rsa

Host minion-01
HostName 10.9.8.6
Port 22
User freebsd
ServerAliveInterval 120
IdentityFile ~/.ssh/id_rsa
```

## Bootstrapping a Salt Master

```sh
$ ./bootstrap/digitalocean/freebsd/10.2/salt-master
Usage: ./bootstrap/digitalocean/freebsd/10.2/salt-master ssh-profile

$ ./bootstrap/digitalocean/freebsd/10.2/salt-master salt
```

## Bootstrapping a Salt Minion

```sh
$ ./bootstrap/digitalocean/freebsd/10.2/salt-minion
Usage: ./bootstrap/digitalocean/freebsd/10.2/salt-minion ssh-profile salt-master

$ ./bootstrap/digitalocean/freebsd/10.2/salt-minion minion-01 10.9.8.7
```
