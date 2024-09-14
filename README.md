# bandit_writeup
# LEVEL 0 → 1
- ssh bandit0@bandit.labs.overthewire.org -p 2220 <br/>
Password : bandit0 <br/>
- ls <br/>
- cat readme<br/>
Password for the next level is obtained<br/>
# LEVEL 1 → 2<br/>
- ssh bandit1@bandit.labs.overthewire.org -p 2220<br/>
Password : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If<br/>
- ls
- cat./-<br/>
This is used to read the file whose filename itself is '-'<br/>
Password for the next level is obtained<br/>
# LEVEL 2 → 3<br/>
- ssh bandit2@bandit.labs.overthewire.org -p 2220<br/>
Password : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx<br/>
- ls -alps
- cat “spaces in this filename” <br/>
To read files with spaces in the name, filename has to be put in quotation marks, or we can use backslash<br/>
Password for the next level is obtained<br/>
# LEVEL 3 → 4<br/>
- ssh bandit3@bandit.labs.overthewire.org -p 2220<br/>
Password : MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx<br/>
- ls -alps<br/>
-	cd inhere/<br/>
-	cat …Hiding-From-You<br/>
Password for the next level is obtained<br/>
# LEVEL 4 → 5<br/>
- ssh bandit4@bandit.labs.overthewire.org -p 2220<br/>
Password : 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ<br/>
- ls -alps<br/>
- cd ls<br/>
- find. -type f | xargs file<br/>
Finding human-readable file in the directory<br/>
-	cat ./-file07<br/>
Password for the next level is obtained<br/>
# LEVEL 5 → 6<br/>
- ssh bandit5@bandit.labs.overthewire.org -p 2220<br/>
Password : 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw<br/>
- ls -alps<br/>
- cd inhere/<br/>
- find . -type f -size 1033c ! -executable<br/>
Finding human-readable, 1033 bytes in size and not executable file<br/>
-	cd maybehere07/<br/>
-	cat ./.file2<br/>
Password for the next level is obtained<br/>
# LEVEL 6 → 7<br/>
- ssh bandit6@bandit.labs.overthewire.org -p 2220<br/>
Password : HWasnPhtq9AVKe0dmk45nxy20cvUa6EG<br/>
-	find / -type f -user bandit7 -group bandit6 -size 33c<br/>
To find the file owned by user bandit7, owned by group bandit6 and is 33 bytes in size<br/>
-	cat /var/lib/dpkg/info/bandit7.password<br/>
Password for the next level is obtained<br/>
# LEVEL 7 → 8<br/>
- ssh bandit7@bandit.labs.overthewire.org -p 2220<br/>
Password : morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj<br/>
-	strings data.txt | grep "millionth"<br/>
To find the password which is present next to the word millionth<br/>
Password for the next level is obtained<br/>
