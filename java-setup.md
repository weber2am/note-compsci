# java for ThinkJava2

For the ThinkJava2 book/class, install openjdk 11.


## OpenJDK 11 Install and Setup

### Raspberry Pi OS

Tony's old pi is based on Debian 9 Stretch, for which openjdk 11 is not available.  
Ann's pi is Debian 10 Buster.  So is Tony's 2nd rpi.  
For those, install and check the jdk like this:
```
$ sudo apt install default-jdk
$ javac -version
javac 11.0.9.1
```


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

## DrJava

Download from `http://drjava.org`.

To run it, navigate in terminal to where it was downloaded.  Then use one of these commands:
```
$ java -jar drjava-rest-of-fname
$ java -jar drjava-rest-of-fname &>/dev/null &
```
The first command keeps that terminal occupied until the drjava window is closed.  The 2nd command separates the drjava window from the terminal, so you can continue using the terminal.
