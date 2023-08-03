## general tips https://tryhackme.com

### how to download files from machines

Problem: you are following a path with an embedded machine containing some files needed for solving the objective (I ran into this problem following the SOC path in the PhishTool room). But the machine has no internet access and the files or the file content can't be transfered through the clipboard. How can we get the files to an attack box?

Solution: let's open a little file server with python.

1. connect to the network (download the openvpn config from tryhackme and connect, see https://tryhackme.com/access) if you want to use your own attack box or start a tryhackme attack box
1. start the machine (e.g. IP 10.10.39.181)
    * ![image](https://github.com/rainbow-unicorns-ctf/public-notes/assets/83313998/e7303796-63c8-407e-99cf-5a97d5ad524e)

1. open a terminal and cd into the directory containing the needed files
1. start the fileserver: `python3 -m http.server 8000`
    * for python 2: `python -m SimpleHTTPServer 8000`
1. using the IP of the machine and the used port (in the example `8000`) we use a webbrowser on the attack box to access the file server, e.g. `http://10.10.39.181:8000/` and can download the files :-)
    * ![image](https://github.com/rainbow-unicorns-ctf/public-notes/assets/83313998/f491b4ff-1cbf-45e0-b914-6ad881c9d80a)

