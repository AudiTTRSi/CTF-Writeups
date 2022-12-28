Advent of Cyber is now regular seasonal room on <a href="https://tryhackme.com/">TryHackMe</a> page.
This is their 4th time and again with awsome story to follow each day's assignment.

Here are my solutions for the Day 13, if anyone gets stuck or need bit of help solving questions.

In today's task main program will be <a href="https://www.wireshark.org/">Wireshark</a>. Wireshark is free and opensource package analyzer which will help us solve today's task.
Before you start answering questions you need to start the VM, which it takes few minutes.
After the VM is booted up you can open trace file which is placed on desktop.
<ol>
  <li><b>Q1</b></li><br>
When you opened the file you can open drop down meanu options <b>Statistics / Protocol Hierarchy</b>. With data from popup window we can answer first question.  
  <li><b>Q2</b></li><br>
We can now close Procotol Analysis window and open <b>Statistics / Conversation</b> under <b>TCP</b> tab where you will find all data to answer second question. 
  <li><b>Q3</b></li><br>
For answering this question you will need to google what service uses this port.  
  <li><b>Q4</b></li><br>
In search/filter bar you write <b>DNS</b> to filter only dns packages and in the packets under <b>Query / Name</b> we can see domain names that were searched. Dont forget to defang answers. Defanging is process to format url in such way that it can't be clcked by accident. You should forget to put in alphabetical order.  
  <li><b>Q5 & Q6 & Q7 & Q8</b></li><br>
We filter by <b>http</b> requests and then we can find answers from 5 to 8.
  <li><b>Q9</b></li><br>
For exporting files from trace we head to <b>File/ Export Objects/ HTPP... </b> and we download the file. For obtaining the hash value of the file can run <blockquote>sha256sum filename</blockquote> and copy part of the output.
  <li><b>Q10</b></li><br>
Open <a href="https://www.virustotal.com/">Virus total</a> and copy hash value of mailcious file and in thab behavour you will find answer to this last question. Dont forget to defang answers.  
</ol>  

I hope anyone who gets stuck finds it helpful<br>
AudiTTRSi
