Advent of Cyber is now regular seasonal room on <a href="https://tryhackme.com/">TryHackMe</a> page.
This is their 4th time and again with awsome story to follow each day's assignment.

Here are my solutions for the Day 14, if anyone gets stuck or need bit of help solving questions.

First you need to boot up VM and attackbox since they will take some time to boot up.

After both VM and attackbox machine are booted up you can open the website on provided ip and port 8080
and log in with credentials provided in description of the task.

Because of vulnerability present in the website applicaton we can freely change ids in the web address and we cycle (changing profile id numbers) through registered users and find answer to the first question.<br>
For second one we copy profile picture and we change id number for images, because profile images have same vulnerability and we can cycle through pictures and we can find the picuter containing flag which is answer of the second question.

I hope anyone who gets stuck finds it helpful<br>
AudiTTRSi
