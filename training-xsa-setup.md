---
layout: default
Comments: true
---

## Settings Host File To Map to HANA XSA System

1.  For Windows OS:
  - Make sure you have admin rights to your machine.
  - Open up Notepad+ or other editor.
  - Go to menu path to run as administrator
  - Open File 
  ```C:\Windows\System32\drivers\etc```
  - Add Entry:
  ```X.X.X.X  hxehost``` and save.
  For Mac, LINUX or other UNIX based machines:
  - With favorite editor open host file with sudo:
  ```sudo edit /etc/hosts```
  or
  ```sudo nano /etc/hosts```
  - Add entry:
  ```X.X.X.X  hxehost``` and then enter sudo password and save.
  - Then flush the cache
  ```sudo killall -HUP mDNSResponder```
  
