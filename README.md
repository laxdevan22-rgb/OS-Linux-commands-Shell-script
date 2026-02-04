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
## OUTPUT
<img width="450" height="148" alt="image" src="https://github.com/user-attachments/assets/76018746-5d2f-4356-b21c-52880ff3b8d2" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="420" height="203" alt="image" src="https://github.com/user-attachments/assets/d5614c93-365f-4ab2-b912-ce68639a3f8e" />

comm file1 file2
 ## OUTPUT
 <img width="521" height="58" alt="image" src="https://github.com/user-attachments/assets/10f8ca6b-47d0-462f-bb87-44508bb29247" />


 
diff file1 file2
## OUTPUT
<img width="534" height="385" alt="image" src="https://github.com/user-attachments/assets/3a834144-4208-4bc3-a23c-c2c28266354e" />


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
<img width="478" height="114" alt="image" src="https://github.com/user-attachments/assets/276f0bfb-34b6-41c8-9c54-023c599d9186" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="544" height="140" alt="image" src="https://github.com/user-attachments/assets/285bb92f-9991-4d01-9f0d-cc5b5c760f9e" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="543" height="134" alt="image" src="https://github.com/user-attachments/assets/f3d468cd-3fc7-411c-94df-6e8bb475da65" />


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
<img width="521" height="63" alt="image" src="https://github.com/user-attachments/assets/14e7faab-e92c-4f26-8ffd-c4dab9313e31" />




grep hello newfile 
## OUTPUT
<img width="489" height="79" alt="image" src="https://github.com/user-attachments/assets/965564ac-37c5-4ed7-a49d-6f02d781ea8f" />




grep -v hello newfile 
## OUTPUT
<img width="538" height="78" alt="image" src="https://github.com/user-attachments/assets/0009b0c0-8b80-41ab-8cb0-b29289ac9e1d" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="686" height="95" alt="image" src="https://github.com/user-attachments/assets/9a8ce86d-7f70-40e7-9296-7b4d8f797421" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="732" height="65" alt="image" src="https://github.com/user-attachments/assets/e8cfaecd-fc2b-4aac-8087-668645cf2e82" />




grep -R ubuntu /etc
## OUTPUT
<img width="764" height="268" alt="image" src="https://github.com/user-attachments/assets/9b08b96c-1040-41f0-91d7-851bbba04262" />




grep -w -n world newfile   
## OUTPUT
<img width="593" height="105" alt="image" src="https://github.com/user-attachments/assets/09ba8e48-e77e-4fda-bb92-73c687625f2e" />


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
<img width="710" height="103" alt="image" src="https://github.com/user-attachments/assets/9fcac5af-08ff-48e9-98aa-f3017d605bcd" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="650" height="106" alt="image" src="https://github.com/user-attachments/assets/d6ce9c77-ed04-4f55-a46f-18a0a0518b7b" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="758" height="106" alt="image" src="https://github.com/user-attachments/assets/20a2cd3b-bae4-4ab7-b846-6c9973ce4c26" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="615" height="75" alt="image" src="https://github.com/user-attachments/assets/a5090601-f6c4-4fc1-af6a-d402fd6d7cd1" />



egrep '(world$)' newfile 
## OUTPUT
<img width="609" height="78" alt="image" src="https://github.com/user-attachments/assets/8838f067-c4f8-49a4-9b78-eeb2ac3653df" />



egrep '(World$)' newfile 
## OUTPUT
<img width="603" height="61" alt="image" src="https://github.com/user-attachments/assets/0545d732-ca75-489f-ac6c-0de4a9eafccc" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="696" height="95" alt="image" src="https://github.com/user-attachments/assets/8eb3b919-31b0-4b57-9780-5d05833f2c43" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="592" height="67" alt="image" src="https://github.com/user-attachments/assets/037aa347-897c-475e-8664-24925c7e7800" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="682" height="71" alt="image" src="https://github.com/user-attachments/assets/278ee247-ca8a-47ee-be8e-48c51165ad24" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="675" height="67" alt="image" src="https://github.com/user-attachments/assets/17496cec-9392-4150-a111-727f3a52b631" />


egrep l{2} newfile
## OUTPUT
<img width="610" height="108" alt="image" src="https://github.com/user-attachments/assets/549f2488-91e3-40ad-b7a1-026824d48ed9" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="606" height="146" alt="image" src="https://github.com/user-attachments/assets/13100856-a21e-4bfe-8b34-b6845c20bb5a" />


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
<img width="564" height="60" alt="image" src="https://github.com/user-attachments/assets/1f066474-2aba-44a4-867a-536135ac90a2" />



sed -n -e '$p' file23
## OUTPUT
<img width="573" height="64" alt="image" src="https://github.com/user-attachments/assets/a516d0b5-857f-40bb-a9e1-2944c8f67331" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="651" height="304" alt="image" src="https://github.com/user-attachments/assets/d8032195-b743-4564-8a80-9edf494f6b99" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="650" height="303" alt="image" src="https://github.com/user-attachments/assets/03752638-4e5a-45c0-bac8-4dcff6d5a114" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="683" height="311" alt="image" src="https://github.com/user-attachments/assets/93a1ad0d-dc00-4629-93c7-1745a74ec6ae" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="593" height="207" alt="image" src="https://github.com/user-attachments/assets/d62b78a3-b616-4174-a6f3-c93855ebf677" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="648" height="142" alt="image" src="https://github.com/user-attachments/assets/9b057bae-a041-4f13-b4e5-43fbd7da36e0" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="696" height="101" alt="image" src="https://github.com/user-attachments/assets/ea8a4da3-2e7e-4f59-8e2c-9fafb5f6d0fb" />



seq 10 
## OUTPUT
<img width="418" height="370" alt="image" src="https://github.com/user-attachments/assets/23863d1f-d56e-4792-bcec-aa1f7dc3f1dc" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="613" height="141" alt="image" src="https://github.com/user-attachments/assets/771b3428-f113-4fdf-9b5a-0a853023fc2c" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="640" height="130" alt="image" src="https://github.com/user-attachments/assets/d47659a3-2327-4ec4-bd75-be26d9416843" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="593" height="167" alt="image" src="https://github.com/user-attachments/assets/b955c606-45cd-46a8-9cd4-fa473e09660f" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="574" height="137" alt="image" src="https://github.com/user-attachments/assets/e44dfdfa-5e6b-40ce-8039-2b4b677cd9e4" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="625" height="134" alt="image" src="https://github.com/user-attachments/assets/8eaff76c-6e9e-44be-bd19-4c77f3ff97b0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="679" height="137" alt="image" src="https://github.com/user-attachments/assets/cd99a78d-22f0-4adf-a1dc-3bf31ca5a9fc" />



sed -n '2,4{s/$/*/;p}' file23
<img width="713" height="141" alt="image" src="https://github.com/user-attachments/assets/6812c93d-d1cf-4225-846b-206d8a4f4a26" />


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
<img width="433" height="203" alt="image" src="https://github.com/user-attachments/assets/647e1d06-2046-4046-8dc9-95426378714f" />


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
<img width="453" height="201" alt="image" src="https://github.com/user-attachments/assets/4dc061ab-6a5c-4de9-b698-41dcf867597d" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="790" height="289" alt="image" src="https://github.com/user-attachments/assets/a49e0eb8-3c2b-44d9-8d81-eb20948b7d6b" />

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


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT



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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT


 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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


# RESULT:
The Commands are executed successfully.
