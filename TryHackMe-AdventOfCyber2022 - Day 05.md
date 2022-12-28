Advent of Cyber is now regular seasonal room on <a href="https://tryhackme.com/">TryHackMe</a> page.
This is their 4th time and again with awsome story to follow each day's assignment.

Here are my solutions for the Day 5, if anyone gets stuck.

<ol>

  <li><b>Q1</b></li><br>
TO scan initial scan of open ports you run nmap scan:
  <blockquote>nmap -sV VM_IP</blockquote>
After that we try bruteforcing the VNC login password with hydra:
  <blockquote>hydra -s 5900 -P /usr/share/wordlists/rockyou.txt VM_IP vnc</blockquote>
  <li><b>Q2</b></li><br>
 We connect to the remote VM with Remmina tool installed on Attackbox with password we got with hydra tool. We can find the flag is written on the desktop background.
</ol>

I hope anyone who gets stuck finds it helpful<br>

AudiTTRSi
