
**Find your local IP Address**

```
ifconfig | grep broadcast | awk '{print $2}'
```

**Find devices on your LAN**

First find your local IP address either with `ifconfig` or with the above command.

With that address, grab the subnet mask (IP base) by taking the first 3 segments i.e. `xxx.xxx.xx` and then append `.0/24` to the end, producing `xxx.xxx.xx.0/24`.

*Run scan:*

```
sudo nmap -sP xxx.xxx.xx.0/24
```

**Basic port scan**

```
nmap -sT <TARGET>
```

**Verbose scan with OS and version detection**

```
nmap -v -A <TARGET>
```

**Vulnerability scan**

```
nmap --script vuln <TARGET>
```

**Subdomain scan**

```
nmap --script dns-brute --script-args dns-brute.domain=<TARGET-DOMAIN>,dns-brute.threads=6,dns-hostlist=<WORDLIST-FILE>
```

**Web server scan**

```
nikto -Display 1234EP -o report.html -Format htm -Tuning 123bde -host <TARGET-DOMAIN>
```
