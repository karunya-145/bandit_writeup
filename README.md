# bandit_writeup

# LEVEL 0 → 1
- ssh bandit0@bandit.labs.overthewire.org -p 2220 <br/>
Password : bandit0 <br/>
- ls <br/>
- cat readme<br/>
To view the contains of the file<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 1 → 2<br/>
- ssh bandit1@bandit.labs.overthewire.org -p 2220<br/>
Password : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If<br/>
- ls<br/>
To view the contents<br/>
- cat./-<br/>
This is used to read the file whose filename itself is '-'<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 2 → 3<br/>
- ssh bandit2@bandit.labs.overthewire.org -p 2220<br/>
Password : 263JGJPfgU6LtdEvgfWU1XP5yac29mFx<br/>
- ls -alps
- cat “spaces in this filename” <br/>
To read files with spaces in the name, filename has to be put in quotation marks, or we can use backslash<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 3 → 4<br/>
- ssh bandit3@bandit.labs.overthewire.org -p 2220<br/>
Password : MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx<br/>
- ls -alps<br/>
-	cd inhere/<br/>
-	cat …Hiding-From-You<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 4 → 5<br/>
- ssh bandit4@bandit.labs.overthewire.org -p 2220<br/>
Password : 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ<br/>
- ls -alps<br/>
- cd ls<br/>
- find. -type f | xargs file<br/>
Finding human-readable file in the directory<br/>
-	cat ./-file07<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 5 → 6<br/>
- ssh bandit5@bandit.labs.overthewire.org -p 2220<br/>
Password : 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw<br/>
- ls -alps<br/>
- cd inhere/<br/>
- find . -type f -size 1033c ! -executable<br/>
Finding human-readable, 1033 bytes in size and not executable file<br/>
-	cd maybehere07/<br/>
-	cat ./.file2<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 6 → 7<br/>
- ssh bandit6@bandit.labs.overthewire.org -p 2220<br/>
Password : HWasnPhtq9AVKe0dmk45nxy20cvUa6EG<br/>
-	find / -type f -user bandit7 -group bandit6 -size 33c<br/>
To find the file owned by user bandit7, owned by group bandit6 and is 33 bytes in size<br/>
-	cat /var/lib/dpkg/info/bandit7.password<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 7 → 8<br/>
- ssh bandit7@bandit.labs.overthewire.org -p 2220<br/>
Password : morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj<br/>
-	strings data.txt | grep "millionth"<br/>
To find the password which is present next to the word millionth<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 8 → 9<br/>
- ssh bandit8@bandit.labs.overthewire.org -p 2220<br/>
Password : dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc<br/>
-	sort data.txt | uniq -c<br/>
To find the line that occurs only once<br/>
<br/>
Password for the next level is that line<br/>
<br/>

# LEVEL 9 → 10<br/>
- ssh bandit9@bandit.labs.overthewire.org -p 2220<br/>
Password : 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM<br/>
-	strings data.txt | grep "="<br/>
To find the line beginning with several '=' characters which is stored in the 'data.txt' file<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 10 → 11<br/>
- ssh bandit10@bandit.labs.overthewire.org -p 2220<br/>
Password : FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey<br/>
- strings data.txt | base64 -d<br/>
To find the content which is a base64 encoded data<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 11 → 12<br/>
- ssh bandit11@bandit.labs.overthewire.org -p 2220<br/>
Password : dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr<br/>
-	cat data.txt<br/>
<br/>
An ecrypted text was displayed which contains the password<br/>
Encrypted text : Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4<br/>
<br/>
It was decrypted using a python program which was written for ROT13<br/>
Decrypted text : The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4<br/>
<br/>
Thus password for the next level is obtained<br/>
<br/>

# LEVEL 12 → 13<br/>
- ssh bandit12@bandit.labs.overthewire.org -p 2220<br/>
Password : 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4<br/>
- ls -alps<br/>
- mkdir /tmp/aaj<br/>
- cp data.txt /tmp/aaj<br/>
- cd /tmp/aaj<br/>
- ls<br/>
- cat data.txt<br/>
- xxd -r data.txt>data<br/>
- ls<br/>
- file data<br/>
- mv data file.gz<br/>
- gzip -d file.gz<br/>
- ls<br/>
- file file<br/>
- mv file file.bz2<br/>
- bzip2 -d file.bz2<br/>
- mv file file.gz<br/>
- gzip -d file.gz<br/>
- file file<br/>
- mv file file.tar<br/>
- tar xf file.tar<br/>
- ls<br/>
- file data5.bin<br/>
- rm file.tar<br/>
- rm data.txt<br/>
- file data5.bin<br/>
- mv data5.bin data.tar<br/>
- tar xf data.tar<br/>
- ls<br/>
- file data6.bin<br/>
- mv data6.bin data.bz2<br/>
- bzip2 -d data.bz2<br/>
- mv data data.tar<br/>
- tar xf data.tar<br/>
- ls<br/>
- mv data8.bin data.gz<br/>
- gzip -d data.gz<br/>
- ls<br/>
- file data<br/>
- cat data<br/>
<br/>
Password for the next level is obtained<br/>
<br/>

# LEVEL 13 → 14<br/>
- ssh bandit13@bandit.labs.overthewire.org -p 2220<br/>
Password : FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
