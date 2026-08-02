
# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT

![output1](./img/output1.png)



cat < file2
## OUTPUT
![output2](./img/output%202.png)


# Comparing Files
cmp file1 file2
## OUTPUT
![output3](./img/output%203.png)

comm file1 file2
 ## OUTPUT
![output4](./img/output4.png)

 
diff file1 file2
## OUTPUT
![output5](./img/output5.png)

#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![output6o](./img/output%206o.png)

cut -d "|" -f 1 file22
## OUTPUT
![output7](./img/output7.png)


cut -d "|" -f 2 file22
## OUTPUT
![output8](./img/output8.png)

cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
![output9o](./img/output9o.png)


grep hello newfile 
## OUTPUT
![output10](./img/output10.png)



grep -v hello newfile 
## OUTPUT
![output11](./img/output11.png)



cat newfile | grep -i "hello"
## OUTPUT
![output12](./img/output12.png)



cat newfile | grep -i -c "hello"
## OUTPUT
![output13](./img/outout13.png)



grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT
![output14](./img/output14.png)


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![output15](./img/output15.png)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![output16](./img/output16.png)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![output17](./img/output17.png)


egrep '(^hello)' newfile 
## OUTPUT
![output18](./img/output18.png)

egrep '(world$)' newfile 
## OUTPUT
![output19](./img/output19.png)


egrep '(World$)' newfile 
## OUTPUT
~![output19](./img/output19.png)



egrep '((W|w)orld$)' newfile 
## OUTPUT
![output20](./img/output20.png)


egrep '[1-9]' newfile 
## OUTPUT
![output22](./img/output22.png)


egrep 'Linux.*world' newfile 
## OUTPUT
![output21](./img/output%2021.png)


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1600" height="533" alt="WhatsApp Image 2026-07-31 at 9 24 40 AM" src="https://github.com/user-attachments/assets/cfa91f29-a31f-4e13-9ad0-e30e138d2242" />



egrep l{2} newfile
## OUTPUT
<img width="1600" height="533" alt="WhatsApp Image 2026-07-31 at 9 40 43 AM" src="https://github.com/user-attachments/assets/a2f01207-b382-494a-b01d-baafb61333a4" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1600" height="533" alt="WhatsApp Image 2026-07-31 at 9 50 32 AM" src="https://github.com/user-attachments/assets/9ba0d75f-48a2-4f65-bc2c-ecbe840a31bc" />
cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
<img width="1890" height="832" alt="image" src="https://github.com/user-attachments/assets/0f1418cd-7de9-4bb9-9364-f5eb6976f686" />



sed -n -e '$p' file23
## OUTPUT
<img width="1589" height="990" alt="WhatsApp Image 2026-07-31 at 10 27 01 PM" src="https://github.com/user-attachments/assets/a3230bc4-a7a6-4fbe-bba7-48d2e7d43aad" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1600" height="800" alt="WhatsApp Image 2026-07-31 at 10 29 21 PM" src="https://github.com/user-attachments/assets/9ddb7ee7-475e-428c-8ab0-e66bc4ad831a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1600" height="541" alt="image" src="https://github.com/user-attachments/assets/487b9088-a514-47c6-99cd-192db7235f18" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1600" height="759" alt="image" src="https://github.com/user-attachments/assets/1d458a65-991e-44aa-b2fa-76352d9afe7a" />





sed -n -e '1,5p' file23
## OUTPUT

<img width="1600" height="533" alt="image" src="https://github.com/user-attachments/assets/a5c0bc23-41f8-4e9c-9e4b-a7dddd87fd2a" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1600" height="553" alt="WhatsApp Image 2026-08-01 at 9 34 11 PM" src="https://github.com/user-attachments/assets/122ae68c-7500-4fa3-ba48-8c4b9b8dcbf2" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1600" height="853" alt="WhatsApp Image 2026-08-01 at 9 35 49 PM" src="https://github.com/user-attachments/assets/15bc7611-dcd9-49fd-bf5d-502c509cb2dc" />



seq 10 
## OUTPUT

<img width="1600" height="853" alt="WhatsApp Image 2026-08-01 at 9 35 49 PM" src="https://github.com/user-attachments/assets/8f1cb4a7-d951-459a-a650-3293cdc9f03c" />



seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1600" height="533" alt="WhatsApp Image 2026-08-01 at 9 41 53 PM" src="https://github.com/user-attachments/assets/69213a19-edef-42ef-af35-046c7790d9f8" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1600" height="533" alt="WhatsApp Image 2026-08-01 at 10 08 24 PM" src="https://github.com/user-attachments/assets/d189da3f-b736-41fd-9083-b377b01bfe6e" />




seq 3 | sed '2a hello'
## OUTPUT


<img width="1600" height="533" alt="WhatsApp Image 2026-08-01 at 10 08 24 PM" src="https://github.com/user-attachments/assets/3f88e8bd-439a-4973-871f-66a42480faaf" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="1600" height="707" alt="WhatsApp Image 2026-08-01 at 10 13 55 PM" src="https://github.com/user-attachments/assets/8b783393-614b-46fb-b4b1-3bfa7f7dd2f6" />


seq 10 | sed '2,9c hello'
## OUTPUT


<img width="1600" height="707" alt="WhatsApp Image 2026-08-01 at 10 13 55 PM" src="https://github.com/user-attachments/assets/e763edd1-8577-4607-8ca1-eb7e6bc00f7a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![seq](./op-img/seq7.png)


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![seq](./op-img/seq8.png)

#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![sort](./op-img/sort1.png)

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT
![sort](./op-img/uniq.png)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![sort](./op-img/tr.png)


cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```


cat urllist.txt | tr -d ' '
 ## OUTPUT
![sort](./op-img/cat1.png)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![sort](./op-img/cat2.png)


#Backup commands

tar -cvf backup.tar *
## OUTPUT
![tar](./op-img/tar1.png)
![tar](./op-img/tar2.png)
![tar](./op-img/tar3.png)
![tar](./op-img/tar4.png)
![tar](./op-img/tar5.png)


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
![tar](./op-img/tvf1.png)
![tar](./op-img/tvf2.png)
![tar](./op-img/tvf3.png)
![tar](./op-img/tvf4.png)


tar -xvf backup.tar
## OUTPUT
![tar](./op-img/xvf1.png)
![tar](./op-img/xvf2.png)


gzip backup.tar

ls .gz
## OUTPUT
 ![tar](./op-img/ls.png)


gunzip backup.tar.gz
## OUTPUT
![tar](./op-img/gunzip.png)
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![tar](./op-img/chmod.png)
 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![tar](./op-img/cat.png)

cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT
![tar](./op-img/chmod1.png)
 
ls file1
## OUTPUT
![ls](./op-img/ls1.png)


echo $?
## OUTPUT 
![echo](./op-img/echo1.png)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
![echo](./op-img/echo2.png)

 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
![str](./op-img/str1.png)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![str](./op-img/strcomp.png)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT
<img width="2172" height="724" alt="image" src="https://github.com/user-attachments/assets/4a03e338-af0d-4fd7-9a50-d9b75c18e2e6" />




# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
<img width="2146" height="732" alt="image" src="https://github.com/user-attachments/assets/21b2da86-c6be-48a9-97d4-317b19fb13db" />



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
<img width="2146" height="732" alt="image" src="https://github.com/user-attachments/assets/9107b79b-5758-4cec-8124-8a3399669ab2" />



# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
## OUTPUT
<img width="2146" height="732" alt="image" src="https://github.com/user-attachments/assets/c847548f-1263-4329-8040-d203e02a3f91" />



# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT

<img width="2079" height="756" alt="image" src="https://github.com/user-attachments/assets/27a20bd9-ba48-428c-aee3-f43ea3a16cd7" />




# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
<img width="1896" height="830" alt="image" src="https://github.com/user-attachments/assets/10f4e128-3f49-4f71-b14f-a84fc447d5c8" />



# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
## OUTPUT
<img width="2039" height="771" alt="image" src="https://github.com/user-attachments/assets/cea13714-966a-4f69-abdf-e69b00df8749" />

 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh

## OUTPUT 
<img width="1920" height="819" alt="image" src="https://github.com/user-attachments/assets/eaed0493-7532-4598-b52e-1de47a57c8fe" />

 
 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
$ ./untiltest.sh

## OUTPUT
<img width="2172" height="724" alt="image" src="https://github.com/user-attachments/assets/9173cdb9-9aaf-4953-a60c-ea95679688b5" />


 
 
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
$ ./forin1.sh

## OUTPUT
<img width="1998" height="787" alt="image" src="https://github.com/user-attachments/assets/3ce0a8d9-5404-4a2b-aef4-b3b0e92da44e" />

 
cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
$ ./forin2.sh

## OUTPUT
<img width="2007" height="784" alt="image" src="https://github.com/user-attachments/assets/e0ff7c4e-aa0d-4b3e-8475-a4fe06255e71" />

 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```

$ chmod 755 forin3.sh
$ ./forin3.sh 

 ## OUTPUT
 <img width="2126" height="740" alt="image" src="https://github.com/user-attachments/assets/d497520f-9aa3-4c28-80e1-ac34671c6f28" />



cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="1828" height="860" alt="image" src="https://github.com/user-attachments/assets/662c3313-02a4-4728-892a-ded89e9cab40" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
$ chmod 755 forctype.sh
$ ./forctype.sh 

## OUTPUT

<img width="2172" height="724" alt="image" src="https://github.com/user-attachments/assets/6a7bf849-0b3a-47fc-b040-40e19c716081" />



cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 

## OUTPUT

<img width="2158" height="729" alt="image" src="https://github.com/user-attachments/assets/4b424b9d-46ee-42ad-809d-8c38c8382323" />



cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
<img width="1915" height="821" alt="image" src="https://github.com/user-attachments/assets/b190a19e-d9c9-4634-9cdf-e275652b6ec6" />

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
## OUTPUT
<img width="2167" height="726" alt="image" src="https://github.com/user-attachments/assets/e2a1eeaa-14da-46e3-8f13-0916e12c201f" />


cat forcontinue.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
<img width="2219" height="709" alt="image" src="https://github.com/user-attachments/assets/cfe10a4b-2b15-4318-b338-f415813d5208" />

 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT
<img width="2080" height="756" alt="image" src="https://github.com/user-attachments/assets/781c88cd-3256-4d81-a33d-8d3966a22a44" />


 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT
./funcex.sh 

<img width="2167" height="726" alt="image" src="https://github.com/user-attachments/assets/daf80f32-cba5-4c4b-aace-b430e22dec59" />

 
./funcex.sh 1 2

<img width="2065" height="762" alt="image" src="https://github.com/user-attachments/assets/cf71c15f-b89d-4789-ac29-15483cb6b2d7" />


cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="1829" height="860" alt="image" src="https://github.com/user-attachments/assets/23f4eb46-925d-4df4-b3e9-b25fd81b2fb3" />


 

cat argshift1.sh
```bash
#/bin/bash 
# store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
# echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3
## OUTPUT
<img width="2194" height="717" alt="image" src="https://github.com/user-attachments/assets/d8297add-220c-4498-bac4-9bd178546c01" />

 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
./argshift.sh 1 2 3
 
<img width="1824" height="862" alt="image" src="https://github.com/user-attachments/assets/a89f3c7a-b7c0-4341-acbd-cba85cb467be" />



cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
<img width="1600" height="759" alt="WhatsApp Image 2026-08-02 at 3 09 56 PM" src="https://github.com/user-attachments/assets/38fa11c4-2168-494f-b96d-92516aebbab6" />



 
cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
<img width="1600" height="534" alt="WhatsApp Image 2026-08-02 at 3 05 50 PM" src="https://github.com/user-attachments/assets/9540f756-a069-4b57-b912-4da598a42751" />


# RESULT:
The Commands are executed successfully.


