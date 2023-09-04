
## Snort modes

### sniffer
sudo snort -d
sudo snort -d -e -v -X

### use local rule
snort -c local.rules -A full

### IPS
sudo snort -c /etc/snort/snort.conf -q -Q --daq afpacket -i eth0:eth1 -A full

rule:
drop any any ...


## rules
```
# ----------------
# LOCAL RULES
# ----------------
# This file intentionally does not come with signatures.  Put your local
# additions here.
# alert tcp any any <> any 21 (msg:"FTP detected";content:"cannot log in";sid:1000001;rev:1)
# alert tcp any 21 <> any any (msg:"FTP detected";content:"cannot log in";sid:1000002;rev:2)
alert tcp any any <> any 21 (msg:"FTP detected";sid:1000001;rev:1)
alert tcp any 21 <> any any (msg:"FTP detected";sid:1000002;rev:2)
```
