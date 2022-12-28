<a href="https://tryhackme.com/room/cowboyhacker">Bounty Hacker</a> is one of easy rooms on TryHackMe.com<br>
I was able to finish it up in couple of minutes with some reference from other similar rooms like this one.

<ol>
<li>First step </li> <br>
  In this step you deploy the target VM and start Attackbox if you dont have it up already. It takes a minute or two to start up.<br><br>
<li>Second step</li><br>
  We use nmap to scan target VM.
  
  <pre>nmap -A -T4 _IP_target_VM</pre> <br>
  Command takes some time to scan and display us back what ports are open. You can see 3 ports open 21 with FTP, 22 ssh and 80 apache server.<br><br>
<li>Third step</li><br>
  As FTP is open and it allows you to connect with anonymous user we try to connect to FTP server on target machine with command:
    <pre>FTP IP_target_VM</pre> <br>
  When prompted for username you enter anonymous. We check what files we can find on server there are 2 files. One cointains note from one user this is also answer to the <b>Q3</b> and other is list of what it looks like passwords. You can download files by command:<br>
  <pre>get file_name</pre> <br>
<li>Forth step</li> <br>
  We will use hydra brute forcing tool to check if any passwords from list we could obtain from FTP server. I used following command:
  <pre>hydra target_VM_IP ssh -l lin -P path_to_the_password_list -s 22 -vV</pre> <br>
  SSH user i used the one i found in file on FTP server.<br><br>
<li>Fifth step</li> <br>
  After Hydra finish its work and you get correct pass you can ssh to the target VM. <br><br>
<li>Sixth step</li> <br>
  When we are logged in server I tried to find user flag and write location of the file into user-flag file:
  <pre>find / -type f -name user.txt 2>/dev/nul > user-flag </pre> <br>
<li>Seventh step</li> <br>
  In this step we check what command can current user run as sudo. We use:
  <pre>sudo -l</pre> <br>
  As we see now only one command we can run. We had over to the <a href="https://gtfobins.github.io/">GTFObins</a> and check what command to run. Copy paste command to the command line and voila we have root access.
<li>Eighth step</li> <br>
  Last step is to find the root.txt file we write its location to root-flag file:
  <pre>find / -type f -name root.txt 2>/dev/null > /tmp/root-flag </pre> <br>
</ol><br>

I hope this helps to the people who might get stucked during solving this room.
