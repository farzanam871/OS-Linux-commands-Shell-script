
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

<img width="940" height="100" alt="image" src="https://github.com/user-attachments/assets/f3579588-3d0f-4ece-a131-9a115c08caf8" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="940" height="72" alt="image" src="https://github.com/user-attachments/assets/c71fb791-1959-40bf-b6a4-bba2049afa8c" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="940" height="72" alt="image" src="https://github.com/user-attachments/assets/3df51b3e-deb1-49a1-b298-b1db2a16d4d0" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/62bc0081-dba3-441c-8e0a-a0a53c87d361" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="940" height="38" alt="image" src="https://github.com/user-attachments/assets/24c7248b-918a-4eab-b51c-a93b2ce361c9" />


seq 10 
## OUTPUT

<img width="940" height="126" alt="image" src="https://github.com/user-attachments/assets/c6f9df4c-c106-4e50-a922-afaf5386b92e" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/63b52eb4-ce1a-464a-b960-951c151b5cbf" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/eba75ab7-7e4a-4332-bd69-88bb30ddd536" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="940" height="58" alt="image" src="https://github.com/user-attachments/assets/b669eb7e-4817-4f09-9f52-2b3554af5789" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="940" height="47" alt="image" src="https://github.com/user-attachments/assets/d3adea8e-6079-40b1-885b-74219767010a" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/5d5998f5-a8ad-4468-8ff4-dcceb2630104" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

```````
<img width="940" height="50" alt="image" src="https://github.com/user-attachments/assets/9319e14d-0b95-4f6c-808b-264b12ba5d1e" />

sed -n '2,4{s/$/*/;p}' file23


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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
```````
<img width="940" height="102" alt="image" src="https://github.com/user-attachments/assets/979e1fc6-0d14-455d-9871-a40cd3a92d84" />


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

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/d7ba5cfd-5491-4f59-a122-cfba02c4d7eb" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="940" height="49" alt="image" src="https://github.com/user-attachments/assets/a6998fa7-d54c-4f8d-a670-3d040b2e94e1" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT




mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="940" height="34" alt="image" src="https://github.com/user-attachments/assets/a36504b3-b49c-4198-b871-e7210bd38dd5" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="940" height="103" alt="image" src="https://github.com/user-attachments/assets/1d64a63c-5c12-45c9-a559-6052a3418ba2" />



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

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/e82f5aeb-41a3-4e2e-bcb7-668bd9fae297" />


 
ls file1
## OUTPUT

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/14075ab7-40ee-4bf9-8809-a6c7b316374b" />


echo $?
## OUTPUT

<img width="940" height="25" alt="image" src="https://github.com/user-attachments/assets/0c5d24d7-c601-4c6d-a633-b0e62dc451c4" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT


 
abcd
 
echo $?
 ## OUTPUT

<img width="940" height="112" alt="image" src="https://github.com/user-attachments/assets/b01b8df4-3c8f-4068-948b-6af5366e290f" />



 
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
##OUTPUT

<img width="940" height="26" alt="image" src="https://github.com/user-attachments/assets/85a23916-bf85-4f66-b2bd-5192cb762b6c" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="940" height="117" alt="image" src="https://github.com/user-attachments/assets/0353d9e8-1144-4148-bb59-b39407f5c903" />



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
##OUTPUT

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
##OUTPUT

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
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
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


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/232fc0f4-e4cc-406e-b203-4a21f1c177d5" />


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

<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/c6ba51e0-d396-4926-958a-5bcb9a6d6e68" />


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

<img width="940" height="174" alt="image" src="https://github.com/user-attachments/assets/a8daae92-738e-4f0d-8870-88035e5a4493" />


 
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
## OUTPUT

<img width="940" height="192" alt="image" src="https://github.com/user-attachments/assets/2b36707e-3542-42e9-9acf-a8f48aa405b3" />


$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
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

<img width="940" height="118" alt="image" src="https://github.com/user-attachments/assets/86818e8d-5897-4731-b176-bde31bab7189" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



$ ./exread1.sh 
 
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

<img width="966" height="214" alt="image" src="https://github.com/user-attachments/assets/021a3267-ba17-4424-a06b-e48b00560f51" />

 ./funcex.sh 

 
 ./funcex.sh 1 2

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT

<img width="940" height="48" alt="image" src="https://github.com/user-attachments/assets/380f7da5-97a7-4ac9-bcb5-4212566a3896" />

$ ./argshift.sh 1 2 3
 
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
## OUTPUT
$ ./argshift.sh 1 2 3
 
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

<img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/da72295e-c67d-40da-8c36-209d3ee10d9d" />

 ./argshift.sh 1 2 3
 
 
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
 <img width="940" height="148" alt="image" src="https://github.com/user-attachments/assets/03467c61-5f9e-4316-9735-bf82e77809f1" />

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
<img width="940" height="343" alt="image" src="https://github.com/user-attachments/assets/5b794817-8779-43f2-9c0e-ee0be087b537" />



# RESULT:
The Commands are executed successfully.
