## vagrant
Lanch ubuntu server on virtual box
```bash
$ cd vagrant/ubuntu-14.04
$ vagrant up
```

Use ssh & scp
```bash
$ vagrant ssh-config --host ubuntu >> ~/.ssh/config
$ ssh ubuntu
Welcome to Ubuntu 14.04.1 LTS (GNU/Linux 3.13.0-39-generic x86_64)
```
```bash
$ echo hello > hello.txt
$ scp hello.txt ubuntu:~/hello.txt
hello.txt        100%    6    0.0KB/s    00:00
```
