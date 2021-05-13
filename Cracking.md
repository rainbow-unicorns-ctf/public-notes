## wordlists

## hascat

## wordlists

+ [ kali wordlist doc ]( https://tools.kali.org/password-attacks/wordlists )

---

+ tools/frameworks have some included, e.g.
  ```SHELL
  /usr/share/metasploit-framework/data/wordlists/password.lst
  ```
  + you can use the wordlists package for symlinks and rockyou list:
    ```BASH
    sudo apt install wordlists
    ls /usr/share/wordlists/
    ```
+ [ cracklib-words ]( https://github.com/cracklib/cracklib/releases/latest )
+ [ SecLists most common ]( https://github.com/danielmiessler/SecLists/tree/master/Passwords/Common-Credentials )

### keepass file

```SHELL
KEEPASS_FILE=keepass.kdbx; keepass2john ${KEEPASS_FILE} | sed "s/${KEEPASS_FILE%%.*}://" > uncracked.hash
hashcat -m 13400 -a 0 -w 1 uncracked.hash cracklib-words
```
