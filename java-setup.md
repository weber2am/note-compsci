# java for ThinkJava2

For the ThinkJava2 book/class, install openjdk 11.

## DrJava



## OpenJDK 11 Install and Setup

### Raspbian

See what Ann's pi is:  `$ cat /etc/os-release`.  
If it is Debian 10 Buster, it comes with openjdk 11.

My pi is based on Debian 9 Stretch, for which openjdk 11 is not available.

### Centos 7

Centos 7 comes with openjdk 7 and 8.  To install openjdk 11:
```
$ sudo yum install java-11-openjdk
$ sudo yum install java-11-openjdk-*
```

To set the machine to use openjdk 11:
```
$ sudo alternatives --config java
$ sudo alternatives --config javac
```

