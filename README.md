Recon Scans done on VM (VM was enabled with simple http web server)

Target IP: 192.168.29.36

Recon scans ran:

quick TCP scan: (top 1000 ports)
nmap -sS -T4 -Pn 192.168.29.36 -oN quick-scan.txt

All port scan:
nmap -sS -T4 -p- -Pn 192.168.29.36 -oN full-scan.txt

service enumeration scan:
nmap -sV -sC 192.168.29.36 -oN service-enum.txt

Rustscan:
rustscan -a 192.168.29.36 -- -sC -sV -oN rustscan.txt


Manual scan for services:

curl -I http://192.168.29.36

nc -zv 192.168.29.36 21

smbclient -L 192.168.29.36	




Target Service: HTTP
Target: Ubuntu VM
Tool plan: curl + gobuster + fuff
Goal: Identify hidden dirs and files, find hidden weak points.