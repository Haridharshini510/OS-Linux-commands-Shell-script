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
<img width="1100" height="264" alt="image" src="https://github.com/user-attachments/assets/c60fdd31-a4ed-4b05-960e-c5d5bb18c278" />



cat < file2
## OUTPUT
<img width="1092" height="314" alt="image" src="https://github.com/user-attachments/assets/a2f024bf-4d8d-45d8-a75f-134176d86c45" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="1092" height="129" alt="image" src="https://github.com/user-attachments/assets/f2b0631f-0a1c-4ded-9757-541d528c5b76" />

diff file1 file2
## OUTPUT
<img width="1092" height="479" alt="image" src="https://github.com/user-attachments/assets/75de4aea-0449-4692-b306-6a3f28974d7a" />


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




cut -d "|" -f 1 file22
## OUTPUT
<img width="1097" height="220" alt="image" src="https://github.com/user-attachments/assets/b41ccc44-62fe-455d-8542-706fb8d9e595" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="1097" height="200" alt="image" src="https://github.com/user-attachments/assets/13b134da-4ab6-49d2-a3a3-d3962955ebb3" />



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
<img width="1097" height="125" alt="image" src="https://github.com/user-attachments/assets/c264e3d4-2aa5-49a0-972c-8dd018899842" />




grep hello newfile 
## OUTPUT
<img width="1094" height="131" alt="image" src="https://github.com/user-attachments/assets/36c195df-f88a-4dc8-83e2-c99902c536c1" />





grep -v hello newfile 
## OUTPUT
<img width="1103" height="138" alt="image" src="https://github.com/user-attachments/assets/a0fb95ff-1650-4d28-a3de-185a03f09322" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="1092" height="179" alt="image" src="https://github.com/user-attachments/assets/3bee52f8-8f18-49fd-b61f-08d5d792ba0e" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1098" height="125" alt="image" src="https://github.com/user-attachments/assets/32ebe1ee-e4ba-4c11-9512-5663c775b4f9" />





grep -R ubuntu /etc
## OUTPUT
<img width="1101" height="299" alt="image" src="https://github.com/user-attachments/assets/647acc1b-4c14-4b54-b703-2b7ec57dd49f" />





grep -w -n world newfile   
## OUTPUT
<img width="1094" height="180" alt="image" src="https://github.com/user-attachments/assets/7203beea-a83a-4ccc-bcee-763a517b0023" />




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
<img width="1094" height="182" alt="image" src="https://github.com/user-attachments/assets/2c44ec68-27b4-4b68-b875-1c6604c9039f" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1099" height="174" alt="image" src="https://github.com/user-attachments/assets/f4287e5b-c5be-49c9-93fd-893017b52383" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="1091" height="179" alt="image" src="https://github.com/user-attachments/assets/269282ec-6cf0-48c0-85f7-0858198fd0f8" />





egrep '(^hello)' newfile 
## OUTPUT
<img width="1094" height="133" alt="image" src="https://github.com/user-attachments/assets/b1d0b699-a18c-4a79-a9c9-ece03e7441f7" />



egrep '(world$)' newfile 
## OUTPUT
<img width="1101" height="162" alt="image" src="https://github.com/user-attachments/assets/7d12f826-fbf1-490c-9a51-188631f04956" />



egrep '(World$)' newfile 
## OUTPUT

<img width="1094" height="129" alt="image" src="https://github.com/user-attachments/assets/b46e9dad-e892-4921-a494-568d23b8828b" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1102" height="273" alt="image" src="https://github.com/user-attachments/assets/167316c8-6d81-4f88-87b7-e83c63cecd04" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="1093" height="132" alt="image" src="https://github.com/user-attachments/assets/968e7a03-4abb-402e-85f3-5f81f505cf3e" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1097" height="127" alt="image" src="https://github.com/user-attachments/assets/d9c0ccaa-a3c2-4a8f-b7bd-18bf6e203773" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1098" height="125" alt="image" src="https://github.com/user-attachments/assets/9d88b8e9-2b5e-44fb-b707-dfd5bdc1895f" />




egrep l{2} newfile
## OUTPUT
<img width="1098" height="170" alt="image" src="https://github.com/user-attachments/assets/861c8334-d651-4727-9f8f-df991af407eb" />




egrep 's{1,2}' newfile
## OUTPUT 
<img width="1102" height="202" alt="image" src="https://github.com/user-attachments/assets/b9cae01d-e406-47fa-85a3-f5b8f806feac" />


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
<img width="1092" height="118" alt="image" src="https://github.com/user-attachments/assets/6f5a9ca6-f006-4b8b-a6d8-3433bacde54a" />




sed -n -e '$p' file23
## OUTPUT
<img width="1095" height="120" alt="image" src="https://github.com/user-attachments/assets/89e456af-5038-4c86-b2b2-17e8ab76ec87" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="1100" height="419" alt="image" src="https://github.com/user-attachments/assets/dbc17af1-aa8f-4a72-9c2c-649912b848c8" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="1105" height="399" alt="image" src="https://github.com/user-attachments/assets/77762765-e2f1-4695-8cb3-0ed597e10f51" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="1087" height="407" alt="image" src="https://github.com/user-attachments/assets/6082c7e3-b9a2-428d-b773-3b9659da85a1" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="1102" height="286" alt="image" src="https://github.com/user-attachments/assets/39859e9b-c5f6-4e1f-aeaf-fb693d08b778" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="1107" height="206" alt="image" src="https://github.com/user-attachments/assets/23a4c507-6ae4-4a57-90c9-e903a2f6f3e0" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1098" height="170" alt="image" src="https://github.com/user-attachments/assets/88bd1d1d-d03b-498d-929f-2622f0295bac" />




seq 10 
## OUTPUT
<img width="1104" height="508" alt="image" src="https://github.com/user-attachments/assets/83fce828-513e-479b-b062-d70788779f18" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1095" height="209" alt="image" src="https://github.com/user-attachments/assets/5f86e2cf-04d0-42d2-9223-1504829f133a" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1091" height="232" alt="image" src="https://github.com/user-attachments/assets/3c7684d6-e672-4980-9f8f-b823120682a6" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="1096" height="225" alt="image" src="https://github.com/user-attachments/assets/d28fefb9-83ac-444f-afbb-702e547195c8" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="1106" height="191" alt="image" src="https://github.com/user-attachments/assets/f4c2e65c-75b0-46cc-9c2b-31e9c7d313b2" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="1104" height="193" alt="image" src="https://github.com/user-attachments/assets/e09fa59a-c414-4b8a-8f89-2409074ffcab" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="1105" height="203" alt="image" src="https://github.com/user-attachments/assets/5d493969-fa67-40ac-ab60-65c8b8a088c4" />




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
<img width="1094" height="285" alt="image" src="https://github.com/user-attachments/assets/19761f71-c7e7-45a9-b1fd-e8780a6a330c" />


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
<img width="1098" height="295" alt="image" src="https://github.com/user-attachments/assets/037426c4-527b-4c12-b4a6-e90f596332fe" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1098" height="411" alt="image" src="https://github.com/user-attachments/assets/4f5968fe-0b5b-408b-951c-9dedf577470f" />


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
<img width="1094" height="206" alt="image" src="https://github.com/user-attachments/assets/7ccb1f76-0266-4698-a07c-09c5f51d714a" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1090" height="201" alt="image" src="https://github.com/user-attachments/assets/5a21d256-4657-4f60-a62a-0441b21798f6" />




#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1100" height="786" alt="image" src="https://github.com/user-attachments/assets/d3c955a8-c20a-4822-acc6-6a000f575530" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1105" height="649" alt="image" src="https://github.com/user-attachments/assets/34be1c5e-ab27-422a-b8af-aa05fd888743" />



tar -xvf backup.tar
## OUTPUT
<img width="1102" height="712" alt="image" src="https://github.com/user-attachments/assets/16a5dc6e-8692-46fd-a45f-1450293eec01" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1098" height="102" alt="image" src="https://github.com/user-attachments/assets/e1431eb2-9f75-4f5c-8dfb-895d6219f005" />

gunzip backup.tar.gz
## OUTPUT
<img width="1098" height="65" alt="image" src="https://github.com/user-attachments/assets/705d6cc2-2990-48a4-b884-3d8489de5051" />


 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1095" height="203" alt="image" src="https://github.com/user-attachments/assets/989f1035-ed43-4b7e-af73-4d70c418d1e5" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1103" height="193" alt="image" src="https://github.com/user-attachments/assets/9d52f80c-18ec-4cfb-bdf1-dbc03fd11ef3" />



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
<img width="1102" height="659" alt="image" src="https://github.com/user-attachments/assets/8f2e83b7-8b2e-4ad7-ae26-829c0d02213d" />


 
ls file1
## OUTPUT
<img width="1101" height="106" alt="image" src="https://github.com/user-attachments/assets/d3334930-5aa4-4e66-b4b6-df1b0d72d601" />

echo $?
## OUTPUT 
<img width="1097" height="119" alt="image" src="https://github.com/user-attachments/assets/346041a4-4f85-4f71-bd8a-6d5594202067" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1099" height="219" alt="image" src="https://github.com/user-attachments/assets/c7ef3107-c5c0-4b61-8fe8-4ef0e8dd5567" />


abcd
 
echo $?
 ## OUTPUT
<img width="1099" height="225" alt="image" src="https://github.com/user-attachments/assets/b67537dd-1bed-491c-b96c-a51fb2d45bf1" />




 
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
<img width="1103" height="447" alt="image" src="https://github.com/user-attachments/assets/b5fcd764-00a5-4c96-9666-91fd7b6c9055" />




chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1093" height="159" alt="image" src="https://github.com/user-attachments/assets/1e73ed74-590f-40ea-88e3-6076d2da1cc9" />


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
<img width="1104" height="121" alt="image" src="https://github.com/user-attachments/assets/54e97948-d65d-4aac-bf6c-cbafad75ff0b" />


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
<img width="1103" height="119" alt="image" src="https://github.com/user-attachments/assets/0973c00f-7edb-47a7-b2bb-d06c9bc67d95" />




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
<img width="1105" height="180" alt="image" src="https://github.com/user-attachments/assets/ccd4499b-12f7-4ecc-b4fb-c235f277bc37" />


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
<img width="1098" height="236" alt="image" src="https://github.com/user-attachments/assets/ffd50186-ebd8-43d7-bf95-ecc528c4c860" />


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
<img width="1104" height="147" alt="image" src="https://github.com/user-attachments/assets/a995d20a-52ab-4448-b937-e0ce4ce53a51" />



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
<img width="1105" height="154" alt="image" src="https://github.com/user-attachments/assets/fa03cbab-53fd-4f5f-aa8b-5e2c1165c992" />


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
<img width="1099" height="125" alt="image" src="https://github.com/user-attachments/assets/188944c0-44b5-4c99-b9ea-f92bfc2deac4" />


 
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
<img width="1104" height="473" alt="image" src="https://github.com/user-attachments/assets/2cad51fa-e89d-4953-9a73-1ed06e09e9e4" />


 
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
<img width="1098" height="318" alt="image" src="https://github.com/user-attachments/assets/5de61803-f235-4cac-b9c1-a35dabe3dcbb" />



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
<img width="1102" height="280" alt="image" src="https://github.com/user-attachments/assets/9d74bc08-1d9d-476f-aac5-577e79a26419" />


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
<img width="1101" height="128" alt="image" src="https://github.com/user-attachments/assets/32c1cdfc-3eff-40f9-8479-1d3f14b779c4" />


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
<img width="1092" height="572" alt="image" src="https://github.com/user-attachments/assets/019dabe7-0a92-45d4-876f-b19860c6455e" />


 
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
<img width="1103" height="177" alt="image" src="https://github.com/user-attachments/assets/02f6f0fe-c87d-4dd5-ab31-e3dc4d7ea98b" />


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
 <img width="1105" height="229" alt="image" src="https://github.com/user-attachments/assets/2cb5e68c-6f87-429e-8a1f-c609fbde8695" />


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
<img width="1096" height="165" alt="image" src="https://github.com/user-attachments/assets/3da03104-2976-4c31-bef2-a312b6571679" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="1092" height="147" alt="image" src="https://github.com/user-attachments/assets/8efc3516-9746-4d67-847b-824227f8bae6" />




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

 <img width="1091" height="233" alt="image" src="https://github.com/user-attachments/assets/16a23d80-92a6-4370-967b-bb3df259e1fb" />


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
 <img width="1099" height="193" alt="image" src="https://github.com/user-attachments/assets/819bef74-f190-44f7-9b83-7d84319a3bb8" />


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
 <img width="1100" height="621" alt="image" src="https://github.com/user-attachments/assets/c251ff4e-bbf7-44cb-98f1-baf44de8473e" />

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
 <img width="1100" height="621" alt="image" src="https://github.com/user-attachments/assets/f07228dd-7f48-43bd-b2a7-516646984994" />

 
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
 <img width="1101" height="625" alt="image" src="https://github.com/user-attachments/assets/afad7c09-fce8-49d3-adc0-10217b88fe56" />


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
<img width="1097" height="754" alt="image" src="https://github.com/user-attachments/assets/0d93ca7f-5bbb-44d9-9fef-4ff29a2a4c6b" />


# RESULT:
The Commands are executed successfully.
