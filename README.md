sshdb - SSH connections manager
---
Simple program created to manage list of ssh connections.

![Interface](gui.gif)

# Installation
download binary
```
curl -L -s https://github.com/trntv/sshdb/releases/download/0.2.0/sshdb -o sshdb
```
or install with ``go get``
```
go get -u github.com/trntv/sshdb
```

for other package managers see: [https://github.com/kevinburke/sshpass](https://github.com/kevinburke/sshpass)
# Features
- add, show, list, remove ssh connections
- supported fields
    - Host
    - Port
    - User
    - Password
    - Key File
- connect to server by key
- database encryption

# Usage
```
NAME:
   sshdb - SSH connections manager

USAGE:
   help [global options] command [command options] [arguments...]

VERSION:
   0.1.0 (build 9c569b6)

AUTHOR:
   Eugene Terentev <eugene@terentev.net>

COMMANDS:
     show     show server information
     list     list all servers from database
     add      adds server to database
     remove   removes server from database
     to       connects to server
     encrypt  encrypt database
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --database value, --db value  Path to database file (default: "$HOME/.sshdbb") [$SSHED_DB_PATH]
   --help, -h                    show help
   --version, -v                 print the version

```

# Tips
to store passwords you need to install sshpass that allows to 
offer a password via SSH

to install it with brew use
```
brew install http://git.io/sshpass.rb
```

TODO:
 - [ ] backup
 - [ ] restore
 - [ ] manage ssh config (view, edit)
 - [ ] additional arguments to ssh command