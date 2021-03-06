# Script for simple configuring firewall based on nftables.
***
### Description: 
This is a written on bash script, which provides you to fast and simple manipulate with nftables firewall. **Requires `nftables` to be installed.**

Current features:
* Block/unblock ipv4 addresses by simple command
* Find and block ipv4 addresses which attack using DDoS
* Block all tcp connections except your ssh IP-address (suitable for fast remote command on DDoS attacks)
* Force/interactive modes; all actions are reversible
### Usage: 
```
snft [command] [parameters]
Available commands:
    -b,  --block          block IP-address,
         [IP-address1] [IP-address2] ...
    -u,  --unblock        unblock IP-address,
         [IP-address1] [IP-address2] ...
    -ba, --block-all      block all connections except the current IP,
         -f, --force      do not request confirmation for actions,
    -d,  --ddos           find and block connections to IP addresses with which the specified number of connections is exceeded,
         -f, --force      do not request confirmation for actions,
         [2-∞]            the connection threshold with an IP address, exceeding which IP address is considered to be an attacker,
    -l,  --list           list of blocked IP-addresses,
    -rr, --reset-rules    reset snft rules,
         -f, --force      do not request confirmation for actions,
         -b, --block      delete rules with manually blocked IP-addresses,
         -ba, --block-all delete blockall rule,
         -d,  --ddos      delete rules created by the ddos parameter,
    -h,  --help           show help and exit.
    -v,  --version        show version information.
