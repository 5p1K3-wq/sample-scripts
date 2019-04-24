# Sample commands Nmap

## Scan one host or individual IP address

### Scan individual IP address
```Bash
$ nmap 192.168.1.1
```
### Scan server by hostname
```Bash
$ nmap <name server>.domain.com
```  
### Increase the Level of Detailing the scan results:
```Bash
$ nmap -v <server name>.<domain name>.com
$ nmap -vv <server name>.<domain name>.com
```

# Scanning Multiple IP Addresses


### Scan Multiple IP Addresses:
```Bash
$ nmap 192.168.1.1 192.168.1.2 192.168.1.3
$ namp 192.168.1.1,2,3
```

### Scan Subnet:
```Bash
$ nmap 192.168.1.0/24
$ nmap 192.168.1.*
```

### Scan the range of IP Addresses (192.168.1.0 - 192.168.1.200):
```Bash
$ nmap 192.168.1.0-200
```

# Search Active Computers on the Net

### Scan the network in search of Active Hosts:
```Bash
$ nmap -sn 192.168.1.0/24
```

# Scanning a List of Hosts from a File

### Scanning the list of hosts / networks from the File:
```Bash
$ nmap -iL input.txt
```


# Exclude IP / Hosts / Networks from Scanning


### Exclude Goals from Nmap scanning:
```Bash
$ nmap 192.168.1.0/24 --exclude 192.168.1.1
$ nmap 192.168.1.0/24 --exclude 192.168.1.1 192.168.1.5
$ nmap 192.168.1.0/24 --exclude 192.168.1.1,2,3
```
### Exclude List of hosts taken from file:
```Bash
$ nmap 192.168.1.0/24 --excludefile exclude.txt
```

# Scanning Specified Ports

### Scan One Port:
```Bash
$ nmap -p 80 192.168.1.1
```
### Scan Multiple Ports:
```Bash
$ nmap -p 80,443 192.168.1.1
```

### Scan Ports Range:
```Bash
$ nmap -p 80-1000 192.168.1.1
```

### Scan All Ports:
```Bash
$ nmap -p "*" 192.168.1.1
```

### Scan some of the Most Common Ports:
```Bash
$ nmap --top-ports 5 192.168.1.1
$ nmap --top-ports 10 192.168.1.1
```
