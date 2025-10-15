<img width="1097" height="127" alt="image" src="https://github.com/user-attachments/assets/0ec7334d-c1a2-4d56-a039-62402311e1dc" /># OS-Linux-commands-Shell-scripting
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
<img width="1096" height="171" alt="image" src="https://github.com/user-attachments/assets/4eb62b2b-7980-48ce-8b01-d9cc01997033" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="1097" height="200" alt="image" src="https://github.com/user-attachments/assets/c2e1f9e4-7624-4e5a-93df-3267448c7108" />


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
<img width="1097" height="220" alt="image" src="https://github.com/user-attachments/assets/db2bce5c-3667-4bbc-8794-1da50d05f0a9" />



grep hello newfile 
## OUTPUT
<img width="1097" height="125" alt="image" src="https://github.com/user-attachments/assets/92312ab7-78ef-477b-a55c-88ff36e2189a" />




grep -v hello newfile 
## OUTPUT
<img width="1103" height="138" alt="image" src="https://github.com/user-attachments/assets/224c49dc-afe1-4153-80a5-36d5dbb4a3cc" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="1092" height="179" alt="image" src="https://github.com/user-attachments/assets/9351eafe-1995-448e-9588-c9c665b63b21" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="1098" height="125" alt="image" src="https://github.com/user-attachments/assets/e2b37bcd-2a72-4e90-bdb7-c1a312c4cad8" />




grep -R ubuntu /etc
## OUTPUT
<img width="1094" height="180" alt="image" src="https://github.com/user-attachments/assets/d0a8df3d-935c-4fd6-83a1-4b3f58466dbe" />



grep -w -n world newfile   
## OUTPUT
<img width="1094" height="182" alt="image" src="https://github.com/user-attachments/assets/99f8e53d-e185-46bd-a0c4-3c3ce6b97af5" />


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
<img width="1099" height="174" alt="image" src="https://github.com/user-attachments/assets/c0bdd124-48e7-4189-bada-ad3578e80707" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="1091" height="179" alt="image" src="https://github.com/user-attachments/assets/c2feb750-ded4-482d-aa57-6ce282501daa" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="1094" height="133" alt="image" src="https://github.com/user-attachments/assets/a1a14900-2331-4161-9384-2250607650e1" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="1101" height="162" alt="image" src="https://github.com/user-attachments/assets/5ccea889-30ed-4035-8a46-622a0f6bf917" />



egrep '(world$)' newfile 
## OUTPUT
<img width="1094" height="129" alt="image" src="https://github.com/user-attachments/assets/3be2b9eb-6b9e-4a80-ae93-577cafe8e61d" />



egrep '(World$)' newfile 
## OUTPUT

<img width="1101" height="299" alt="image" src="https://github.com/user-attachments/assets/69dfee0d-ad10-40e7-8672-d4bf18ba90c3" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="1093" height="132" alt="image" src="https://github.com/user-attachments/assets/28f0c67c-1b87-450b-9e83-7f3ecdb0b521" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="1102" height="273" alt="image" src="https://github.com/user-attachments/assets/9fb5ffc3-ed5a-45a6-a5ef-d601eb117da2" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="1098" height="125" alt="image" src="https://github.com/user-attachments/assets/17c13bfc-c12d-4217-9b3a-6d4225261578" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="1098" height="125" alt="image" src="https://github.com/user-attachments/assets/c7b418c9-0293-4eea-8b41-3f24bc91ec71" />



egrep l{2} newfile
## OUTPUT
<img width="1098" height="170" alt="image" src="https://github.com/user-attachments/assets/a65cc4e9-1abc-4e26-9cea-1a67729c75fe" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="1102" height="202" alt="image" src="https://github.com/user-attachments/assets/34907bd3-1cc5-4ee9-8a41-ae663ed0889a" />


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
<img width="1092" height="118" alt="image" src="https://github.com/user-attachments/assets/785ea8fe-3823-4359-82ec-f7f5c51feec6" />



sed -n -e '$p' file23
## OUTPUT
<img width="1095" height="120" alt="image" src="https://github.com/user-attachments/assets/afa4c859-debf-4cef-bace-939dc506e4e7" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT



sed  -e '2s/Ram/Sita/' file23
## OUTPUT



sed  '/tom/s/5000/6000/' file23
## OUTPUT



sed -n -e '1,5p' file23
## OUTPUT



sed -n -e '2,/Joe/p' file23
## OUTPUT




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="1095" height="209" alt="image" src="https://github.com/user-attachments/assets/d192d20e-e64c-4df3-803f-2ea015f8da09" />



seq 10 
## OUTPUT



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="1105" height="399" alt="image" src="https://github.com/user-attachments/assets/ef4e7f61-d2f4-4c88-a966-97920e8fe0e3" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="1104" height="508" alt="image" src="https://github.com/user-attachments/assets/a1aa6266-31f0-4979-a70f-6a9248fb756f" />



seq 3 | sed '2a hello'
## OUTPUT



seq 2 | sed '2i hello'
## OUTPUT


seq 10 | sed '2,9c hello'
## OUTPUT


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT




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
<img width="1094" height="206" alt="image" src="https://github.com/user-attachments/assets/eeafdd67-b583-462c-aad3-7875e4b0ad8e" />

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
<img width="1094" height="285" alt="image" src="https://github.com/user-attachments/assets/004cbc55-db53-4c20-91b2-6d51e900a477" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1098" height="295" alt="image" src="https://github.com/user-attachments/assets/44f27823-3107-42d3-aaef-32a98f43fbb7" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1105" height="203" alt="image" src="https://github.com/user-attachments/assets/ff2330ad-13cc-414f-bb2c-9aa84dd96415" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1098" height="411" alt="image" src="https://github.com/user-attachments/assets/8b9248e2-5b41-4886-bbb2-8dcb3f2b8218" />


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 <img width="1098" height="102" alt="image" src="https://github.com/user-attachments/assets/dc3d2304-342a-4a8f-8dde-4f0a2e043367" />

gunzip backup.tar.gz
## OUTPUT
<img width="1097" height="119" alt="image" src="https://github.com/user-attachments/assets/7ba79a78-a95a-4f49-b841-94f56db27830" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1101" height="106" alt="image" src="https://github.com/user-attachments/assets/dd03df5c-e4de-47bb-9cf0-e3ded671973e" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1103" height="193" alt="image" src="https://github.com/user-attachments/assets/3d4b96c1-d63a-46ee-a4f6-c5f9f7aa939d" />


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
<img width="1095" height="203" alt="image" src="https://github.com/user-attachments/assets/e164c941-fe17-4d0f-b395-a7d538f32a4e" />

 
ls file1
## OUTPUT

echo $?
## OUTPUT 

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1102" height="659" alt="image" src="https://github.com/user-attachments/assets/ffb64f95-b460-4cdc-a284-58a8db948e2c" />

abcd
 
echo $?
 ## OUTPUT
<img width="1102" height="712" alt="image" src="https://github.com/user-attachments/assets/07183a0b-b9af-44bb-b06e-59f038308890" />


 
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
<img width="1103" height="447" alt="image" src="https://github.com/user-attachments/assets/db29620f-8a37-43f7-8728-6e5765d9de92" />



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
<img width="1099" height="225" alt="image" src="https://github.com/user-attachments/assets/d2a166d6-1262-4aa9-bfa2-4a5ab59fd6f3" />

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
<img width="1103" height="119" alt="image" src="https://github.com/user-attachments/assets/a8320b07-9c4c-4bb9-b297-b06268e88c6d" />



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
<img width="1105" height="180" alt="image" src="https://github.com/user-attachments/assets/0fc891b3-1cb0-44ed-9ec8-c026bb57c9ea" />

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
<img width="1098" height="236" alt="image" src="https://github.com/user-attachments/assets/45e9a7de-e453-480f-bbe6-4e70e7ea73bd" />

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
<img width="1105" height="180" alt="image" src="https://github.com/user-attachments/assets/4935707e-bc0e-4b2a-a315-4e3ff4f14b53" />


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
<img width="1105" height="154" alt="image" src="https://github.com/user-attachments/assets/d61ed7eb-824d-4d71-a851-7190a43a7e85" />

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
<img width="1099" height="125" alt="image" src="https://github.com/user-attachments/assets/dd51d088-a02d-4e89-9b25-6154d432de98" />

 
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
 <img width="1104" height="473" alt="image" src="https://github.com/user-attachments/assets/ca64d0df-137c-43fb-8d82-5678c4c43da2" />

 
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
<img width="1098" height="318" alt="image" src="https://github.com/user-attachments/assets/75301a89-8ca8-4ff6-a857-a7f6ca4360f9" />


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
<img width="1101" height="128" alt="image" src="https://github.com/user-attachments/assets/28c8d8ca-32bf-434d-b147-f3876acb0220" />

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
<img width="1102" height="280" alt="image" src="https://github.com/user-attachments/assets/122fdf47-fa3c-44f2-89ca-ebfe0ffbcedc" />

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
<img width="1092" height="572" alt="image" src="https://github.com/user-attachments/assets/074c7904-f53d-4bce-a90c-3fdefd546fc4" />

 
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
<img width="1103" height="177" alt="image" src="https://github.com/user-attachments/assets/1a878e96-fe73-4bd8-b3bd-b7ffb7272ea6" />

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
 <img width="1105" height="229" alt="image" src="https://github.com/user-attachments/assets/c89238d1-4a46-4d33-b367-126db54b176f" />

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
<img width="1096" height="165" alt="image" src="https://github.com/user-attachments/assets/e4cb03d5-1e85-4d4a-a9da-47aff3570e40" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="1092" height="147" alt="image" src="https://github.com/user-attachments/assets/af0dc45d-9ef7-4ad9-b11b-bc659871bbdd" />



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

 <img width="1091" height="233" alt="image" src="https://github.com/user-attachments/assets/8b6ff2a1-67ce-4982-9095-e725182fe610" />

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
 <img width="1099" height="193" alt="image" src="https://github.com/user-attachments/assets/3dc6f183-7ecd-4f61-a77b-246add75f6fa" />

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
 <img width="1101" height="625" alt="image" src="https://github.com/user-attachments/assets/92214089-48c6-42b6-9d93-7f38ca5d8c65" />

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
<img width="1097" height="754" alt="image" src="https://github.com/user-attachments/assets/60912f54-7d0b-491e-8a33-39f3fee5a6c4" />


# RESULT:
The Commands are executed successfully.
