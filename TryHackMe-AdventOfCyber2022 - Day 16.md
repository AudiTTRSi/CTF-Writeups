<a href="https://tryhackme.com/room/adventofcyber4">Advent of Cyber</a> is now regular seasonal room on <a href="https://tryhackme.com/">TryHackMe</a> page.
This is their 4th time and again with awsome story to follow each day's assignment.

Today's task (day 16) covers topic of SQL Injection (SQLi).
SQL injection is the placement of malicious code in SQL statements, via web page input.
Attackers will most probably try to querry the database return all of the users and passwords of the application if this vulnerability exist.

Before you start with solving task you need to boot up VM in the task and attackbox for accessing the page. It will probably take a minute or two to boot up.
After that we can open link to the developer page of the app we will try to fix. We login with provided credentials.
<ol>
  <li><b>Question 1 - Fixing SQLi by Data Type Validation</b></li>
First we use fix from description of the task to fix first and then second querry in the elf.php file after we have saved and press run we will get the first flag  
  <li><b>Question 2 - Fixing SQLi Using Prepared Statements</b></li>
With prepared statment described in the task we can quickly fix the <b>search_toys.php</b> and get second flag.
  
  <li>Question 3</li>
To find the third flag we need to fix <b>toy.php</b> we can easly fix it same way we fix the <b>elf.php</b> with data type validation.
  
  <li>Question 4</li>
For fixing the 4th vunlerability and getting forth flag we will need to fix the <b>login.php</b>. We do it with prepared statment as we did with second flag. Just make sure you use $username and $password instead of $q
</ol>  

I hope anyone who gets stuck finds it helpful<br>
AudiTTRSi
