hosts
======

This is a basic perl script to help manage entries in a local hosts file. It was
built for me to easily add, remove, comment, and uncomment entries in the hosts
file of my Windows 10 machine. Hoever, it is easily adaptable for unix/linux systems.

#### Running on Windows 10

By default, it is set up to work on a Windows 10 platform from within the linux
subsystem. You will need to be comfortable installing and using the linux subsystem
to use this script in its default state.

#### Running on Unix/Linux

To run this on a unix/linux system, you will need to modify the $hosts_file and $newline
variables to match your system. Generally, these values would be "/etc/hosts" and "\n"
respectively.

#### Installing

Assuming that Windows users are using the linux subsystem, the installation instructions
are the same regardless of your platform.

```
$ git clone https://github.com/bartobri/hosts.git
$ cd ./hosts
$ sudo cp hosts /usr/local/bin/
```

#### Usage

hosts needs to be run as root, so always use sudo.

Dump the hosts file:
```
$ sudo hosts show
```

Add a new host entry
```
$ sudo hosts add newhost.com
```

Remove an existing host entry
```
$ sudo hosts rm newhost.com
```

Comment an existing hosts entry
```
$ sudo hosts stop newhost.com
```

Uncomment an existing hosts entry
```
$ sudo hosts start newhost.com
```