## links

### learning 

#### ebooks/reading

https://book.hacktricks.xyz/

https://www.yeahhub.com/bruteforce-ssh-using-hydra-ncrack-medusa-kali-linux-2017/



#### platforms

https://cryptopals.com/

https://www.reversinghero.com/

### online tools

[ https://gchq.github.io/CyberChef ]( https://gchq.github.io/CyberChef/#recipe=Magic(4,false,false,'')From_Base64('A-Za-z0-9%2B/%3D',true/disabled)Magic(4,true,true,'HTB%7B'/disabled)Strings('Single%20byte',4,'Alphanumeric%20%2B%20punctuation%20(A)',false/disabled)&input=TlZDaWpGN242cGVNN2E3eUxZUFpyUGdIbVdVSGk5N0xDQXpYeFNFVXJhS21l )

http://www.quipqiup.com/

https://cloud.binary.ninja/

https://www.decompiler.com/




### tools

https://github.com/icsharpcode/AvaloniaILSpy

https://github.com/dnSpy/dnSpy

https://docs.pwntools.com/en/latest/flag.html

https://github.com/internetwache/GitTools

https://github.com/rizinorg/cutter

https://github.com/volatilityfoundation/volatility

### libs/packages

[ impacket ]( https://github.com/SecureAuthCorp/impacket/releases )
* collection of Python classes for working with network protocols

### scripts/snippets

```SHELL
# extract_android_backup.sh
( printf "\x1f\x8b\x08\x00\x00\x00\x00\x00" ; tail -c +25 backup.ab ) |  tar xfvz -
```

```SHELL
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 malfind
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 volshell
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 connections
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 netscan
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 volshell
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 procdump --pid=2752 -n --dump-dir=.
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 procdump --pid=2752 -n --dump-dir .
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 procdump --pid=2752 -n 
volatility --profile=Win7SP1x64 procdump --pid=2752 -n --dump-dir=. -f flounder-pc-memdump.elf
volatility --profile=Win7SP1x64 procdump --pid=2752 --dump-dir=. -f flounder-pc-memdump.elf
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 cmdline
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 consoles
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 filescan
volatility -f flounder-pc-memdump.elf --profile=Win7SP1x64 filescan | grep resume
volatility --profile=Win7SP1x64 dumpfiles -Q 0x000000001e1f6200 --dump-dir=. -f flounder-pc-memdump.elf
```
