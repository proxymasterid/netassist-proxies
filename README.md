# netassist-proxies
A simple shell script for deploying your owns IPv6 proxies via netassist
# How it works

The script establishes 6to4 tunnels. You connect to your server's ipv4 address on a specific port and output one of the ipv6 addresses from your subnet.

## Features

-   Supported networks: `/48`, `/64` but on netassist Only /48 available
-   Connection protocols: `http(s)` / `socks5`
-   Authentication by username and password (or w/o auth)
-   Custom port numbering (from start)
-   Simultaneous online over 60000 proxies
-   Minor resource usage (1000 online proxies = ~ 50mb ram)
-   Auto generating tunnels list

# Installation

```
sudo bash -c "$(wget -qO- https://raw.githubusercontent.com/astridytb/netassist-proxies/main/configure.sh)"
```

# How to start

0. Create account on http://tb.netassist.ua
1. Prepare your own server with a Debian based os.
   It's much better if you only use the server for your proxies and nothing more, because this script changes some system configurations that may affect your other applications. Cheap VPS servers are a great choice.
2. [Create New Tunnel](http://tb.netassist.ua?tid=762030#:~:text=Create%20New%20Tunnel)
3. Install the script on your server with [one simple command](https://github.com/astridytb/netassist-proxies/blob/main/README.md#installation)
4. After installation, the server will be rebooted
5. The list of tunnels is located in your home directory (~/tunnels.txt)

# Requirements

-   Debian based os (tested: Debian 9-11, Ubuntu 18-22)
-   1 CPU, 256 MB RAM
-   The ability to connect to ipv6 addresses
    -   Check: `ping6 -c3 google.com &>/dev/null && echo "Connected successfully" || echo "Connection error"`

# Used

-   [3proxy](https://github.com/z3APA3A/3proxy)
-   [ndppd](https://github.com/DanielAdolfsson/ndppd)

# My Youtube Channel where I share full tutorial
- https://www.youtube.com/channel/UCrQbGvokE9m3LDpOCF9fwng
# My Website where I share free premium ipv6 proxy
- https://proxymaster.my.id

#little donate for vps
https://datalix.de/cp/donate/githubdonation

# Suggestions

If you have any suggestions, please contact me:

-   Email: astridmariskaytb@gmail.com

Please don't spam me with questions.
