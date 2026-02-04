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

<img width="536" height="113" alt="542559014-5882a646-3e56-4850-a777-330f79d26167" src="https://github.com/user-attachments/assets/d9148edc-8d85-45cf-8b0c-553938a6c1fd" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="664" height="109" alt="542559184-c8983baa-46c6-4701-8385-83c28a0f9729" src="https://github.com/user-attachments/assets/9de68229-c05b-41f7-b24e-a63887754cad" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="304" height="149" alt="542559637-55bcdaac-ce8f-454c-b03a-0a4acc67b340" src="https://github.com/user-attachments/assets/8779ba7c-7d97-424a-9a53-9e9a343d78b2" />



tar -xvf.tar
## OUTPUT
<img width="474" height="163" alt="542559753-0b7cdd78-4d1f-4c8b-ad3e-aa1ebef8d89a" src="https://github.com/user-attachments/assets/41047c7f-3eec-40f9-8e54-c817a738e3f1" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="784" height="162" alt="542559942-bdcc8b8c-6850-4b66-831d-b35863bb8c8c" src="https://github.com/user-attachments/assets/09d5dc96-1326-4f48-8545-f414d47d386d" />

 
gunzip backup.tar.gz
## OUTPUT

 <img width="796" height="244" alt="542560113-34320357-c859-4d4b-85df-f14b2709b19a" src="https://github.com/user-attachments/assets/d78bb959-5bfe-410e-816f-30307c0be643" />

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 <img width="785" height="335" alt="542560780-3800b4a7-342f-4a5e-974c-6e2db4732a3e" src="https://github.com/user-attachments/assets/d577e5ad-f514-4c66-a60f-efb308ac5d61" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="396" height="109" alt="542560913-321eb3fc-4d64-4031-8169-e2c3a747ad2a" src="https://github.com/user-attachments/assets/97dec981-9957-4c8c-a54b-8814b9a5e05e" />

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
<img width="454" height="411" alt="542561156-0a5100c8-9a45-4e18-ab19-1edb11c3c53c" src="https://github.com/user-attachments/assets/80beb979-0396-4a95-a153-f827770c2a66" />
UTPUT

 
ls file1
## OUTPUT
<img width="274" height="55" alt="542561975-a51a7181-fb60-4f6a-b1cb-47a5f6d8ad99" src="https://github.com/user-attachments/assets/b8334bbb-a25e-495e-8820-99b77384696d" />

echo $?
## OUTPUT 
<img width="290" height="56" alt="542562107-92328f3a-eaff-4f77-9db1-606eb7a57d97" src="https://github.com/user-attachments/assets/cbf8fea3-1be0-45f2-be48-98739afebce2" />

./one bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="265" height="64" alt="542562200-a966ec46-4286-42ef-9722-6d0346425800" src="https://github.com/user-attachments/assets/4c2b8c61-0f4d-4daf-8cc6-6fe29c78048d" />

abcd
 
echo $?
 ## OUTPUT


 <img width="557" height="268" alt="542562309-b7a99be2-0cc4-4011-8697-3cfc59cbdd34" src="https://github.com/user-attachments/assets/48d4f3eb-8a95-4133-8191-97de50beca64" />

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



<img width="542" height="299" alt="542562576-f0bea342-f4cf-4341-9abc-daeb93c5bbd6" src="https://github.com/user-attachments/assets/1df8ad43-621e-4571-be68-7cf6ffcf0c61" />
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="725" height="222" alt="542563259-8961b0c2-fbc7-4548-9181-d5b59a9fbf89" src="https://github.com/user-attachments/assets/bc91cb4e-0141-4bd3-8b6f-d44d8b2645fd" />


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
<img width="751" height="307" alt="542563418-0432c471-f482-4b42-814d-aee006359f27" src="https://github.com/user-attachments/assets/fb5787d0-0fad-4cc5-a6ee-e2a2d3b07cd5" />

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
<img width="605" height="583" alt="542568013-25079b6d-eebe-44fd-ba69-e241e67fcfc9" src="https://github.com/user-attachments/assets/48c87faa-bcfc-4cb1-b613-82b5a98299a6" />



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
<img width="579" height="473" alt="542568627-f06640fd-f1ce-4a96-a4e6-35be1576c0aa" src="https://github.com/user-attachments/assets/aab75f99-924d-4bee-9b45-cd9536e043a0" />


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
<img width="587" height="582" alt="542566198-225ebb4a-1e9a-45bd-8d68-2ccb5e922fa4" src="https://github.com/user-attachments/assets/8c8036a6-45b4-47dc-bbab-2eabef09512e" />


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
<img width="690" height="571" alt="542565568-d33f1c50-d881-458e-8b8d-cea4bd25bca3" src="https://github.com/user-attachments/assets/47499a2f-ff4c-4c63-ab60-5fe58fe96fe7" />


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
<img width="584" height="298" alt="542568836-638cdc05-5a90-4712-b6bb-2cc82e05d4e4" src="https://github.com/user-attachments/assets/b92f1268-0338-440b-a02c-5b8ac29e9b2d" />


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
<img width="599" height="193" alt="542569084-de818b94-8943-4fc7-a668-5da06a6145e1" src="https://github.com/user-attachments/assets/5d295aff-e4b-4975-b2da-3e97290c3c9e" />
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
<img width="452" height="246" alt="542569424-596df5c1-4b45-4792-91e6-faa759cd38fc" src="https://github.com/user-attachments/assets/0aa8df00-f9cb-4ffa-997e-c41b81c1ff5d" />


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
<img width="461" height="243" alt="542569571-05353b6d-8fcb-442f-8eec-2564719d7968" src="https://github.com/user-attachments/assets/f6e9f4e9-5e75-4e53-b28d-a88d868d1fd0" />


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
<img width="448" height="243" alt="542570259-d6b3390a-8c69-4bc1-95ab-e186770e52c0" src="https://github.com/user-attachments/assets/3704b69f-3260-4902-9d90-7395fdee7dfc" />


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
<img width="782" height="309" alt="542571515-5dad65af-c42b-432e-9651-8054e24496ce" src="https://github.com/user-attachments/assets/5fc1adf7-a383-456d-94e1-1706f819df09" />
 
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
<img width="791" height="305" alt="542571229-ac7dac85-b644-47e2-aee8-d0c83a813f78" src="https://github.com/user-attachments/assets/0b39075c-ee70-4336-9732-297a7409cbeb" />

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
 <img width="517" height="282" alt="542572007-6c7795d6-0b1a-4ad7-8791-3b0b4a8635b2" src="https://github.com/user-attachments/assets/ae0d7a24-8c4e-4f9b-ac68-8128de508a1d" />
 
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
<img width="526" height="172" alt="542572197-1e43f84c-860a-49b6-82bc-ff0ca999af6c" src="https://github.com/user-attachments/assets/1492f761-996a-4e1f-b52a-b7c79ad93057" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT


<img width="471" height="135" alt="542572440-0730db2b-5b2a-4990-ac0a-c014e0e41613" src="https://github.com/user-attachments/assets/816b1542-13ff-44b6-8aff-60d66f977eb4" />

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
<img width="336" height="39" alt="542572644-6bffb717-2f59-483e-a9cb-2677f1902e4d" src="https://github.com/user-attachments/assets/f13ac471-8600-45ed-bb53-6510f3a7dfbf" />

 
 ./funcex.sh 1 2
<img width="313" height="35" alt="542572710-906f3b61-20ad-4fec-9d11-4b38a2e92f77" src="https://github.com/user-attachments/assets/27498716-0b04-4a8c-9f08-352861a208a3" />

 
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
<img width="373" height="59" alt="542572915-88fc4c82-b9e6-4399-b71e-8cc18cd4369d" src="https://github.com/user-attachments/assets/d0880540-0465-4316-982f-e3a10bb734c0" />

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
<img width="338" height="87" alt="542573066-d4b5d672-4fcf-46a7-a7d2-ccc1620171e1" src="https://github.com/user-attachments/assets/ae4dfe31-3af4-48ae-869e-57c00c4bd5d6" />



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
<img width="310" height="335" alt="542573222-c330675a-314f-4f07-ab2e-05f7b8d2e778" src="https://github.com/user-attachments/assets/3f66b74c-8186-4b4c-a588-896fa6ac2cb9" />



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
<img width="298" height="225" alt="542573426-9916b7ee-cb7e-4544-aac0-8b11bf954eb0" src="https://github.com/user-attachments/assets/a5d3c3a9-9fc4-40ba-9e9a-3541fc79172e" /> 
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
<img width="772" height="63" alt="542573537-ef770228-fead-4c42-b129-fb10b49f1720" src="https://github.com/user-attachments/assets/0837a29b-ddb2-46b4-8cb1-0f4d3a8f31b2" />


# RESULT:
The Commands are executed successfully.
