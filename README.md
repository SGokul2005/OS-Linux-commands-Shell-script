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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/e15ddc2d-dd4a-4d0f-896a-96fd5ee8294a)



cat < file2
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/e8e7a02f-a82a-43df-a11f-b2b8bd624800)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/e8de8ea4-d09d-4706-a2ac-31c7d2406115)

comm file1 file2
 ## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/a0142c9e-23b0-4d30-82d1-bdec886366b4)

 
diff file1 file2
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/fb4648fd-80f1-4a71-9482-b4e4cc71baae)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/34853b72-1e98-4758-bf58-2b0b7c878439)




cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/1ba00246-cff1-4d1b-b4c8-b09833f00ab1)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/ba6665dc-3d92-4380-a181-7e5af523ed06)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/8d9c17dc-c0a1-4007-a0a9-f078051bc2f4)



grep hello newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/3d3fddcf-f4ea-4fcd-ad3b-1f79d696d4b8)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/d982aa5b-649b-4312-8111-74f4965fa79b)



cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/6a169f34-13ca-4128-b010-2b2073fafc5c)




cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/7888c9ef-adca-446f-9342-5192573378d8)




grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/6bd16c88-6f18-4906-a7b2-4c34f27cf81c)



grep -w -n world newfile   
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/9574121e-45e1-4ea3-abf3-04290fdf4482)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/f935cfb6-3fd1-4501-871e-aaa6c950881d)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/e40ff0b9-4fa8-4112-a04b-4fa137e5308c)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/0ee2e96a-40ff-4025-beac-b49caab85f93)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/992ada75-2beb-4902-911f-853235b30ef4)



egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/f4807fcb-751a-400e-80a1-f33b5dc9fb04)



egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/1c69c746-9a72-44b3-bf64-65abdd1331ae)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/1bf3de84-86e4-42a1-b559-e610cba59cc9)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/1e1f27a7-e657-4c64-b64d-1848501c191d)



egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/2c9f44f0-70ab-456e-99aa-7b4d699455e9)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/d0c79ea3-23ec-4bcb-ab5f-897131cb7d6e)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/eed94d7f-5ac0-4335-9767-f372030e9079)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/6e360ae6-6084-48e8-884f-1588f283d3c9)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/799429cd-8691-4d12-ad3c-dd600d4c6a5e)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/49a3e01f-0e8e-4bc0-8a46-9e89a6e6b042)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/1c09ecdf-04e3-4201-97f8-d5202e4df665)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/ac06459b-fbea-4bed-8e7b-69c24f72c256)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/9d69dc16-f29d-4e93-b710-6da4de71a701)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/5235d0a2-ab49-4aa5-bbf2-e6c7146fa67c)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/5797b3d4-9337-4f2e-994b-c769c18eb27d)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/ad0d5571-6d82-4717-8d25-987a6793ee5c)



seq 10 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/75f34daa-8140-4d84-a56b-2e41cbd9a683)



seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/3d154d39-cccd-4567-a899-2638e6a5684c)



seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/42381c98-f472-4ab1-8cee-2aa44f042a91)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/351c9bd2-e5b0-47c5-bae8-a8bf57cc79c5)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/c5615e24-59ff-48f0-9a67-7428894063cb)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/c789a581-9913-4dcc-95b4-7a16a84f1e0d)



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/f8ca166d-39bd-42bb-a739-c911c09041bf)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/76123646-c3e0-4c43-af20-37f3bad8ba26)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/61b7a8bc-ca9d-4718-b056-bfb3b3a664d7)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/9c3edd1f-3196-4100-974a-3dbe9becac87)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/f55b66d7-b37b-45ac-86d2-364f60fcd86b)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/6327f12c-7ba9-495b-a030-f08ee2005aa9)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/296047c6-c44b-4861-8f7e-eb1331e737f0)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/bbd126da-8617-45fe-83ef-927f44fe423e)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar

tar -xvf backup.tar
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/444fdbc3-092e-4aa4-909c-b295a840a261)

gzip backup.tar
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/4512c296-ae4a-4fe2-8475-b93c1796d3af)

ls .gz
## OUTPUT
 ![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/15f33edb-1515-4720-9ab1-6bfc5e446971)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/640ad37c-f58e-42b1-b233-bd20fc6b30cc)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/0ebed432-94bb-4b52-94a6-afeac00d597c)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/f763b8ac-7d03-434d-9f5d-0153c63a3e15)

 
ls file1
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/7c322862-454f-460a-aef8-fdff65ebbb20)


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/bbac9f3a-6530-4d30-8d49-e853310f2d28)
 
echo $?
## OUTPUT 
 ![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/85f42444-d17e-4f08-8475-fccf5f75ab6f)

abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/e9b5efec-c01b-4092-b112-7e1a13dbe0d3)


 
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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/0d2f3c39-acc3-48d7-a8fd-2b178d8e96cc)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/754be8f7-f1f7-4eff-85ae-062aa4b53fb0)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/8551b5e3-e91e-430b-8433-b42dd64550ed)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/b27cb9e3-0b23-4680-844d-715c27276211)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/4eb3d096-5b6e-49d1-8833-4a1ddf3ab6de)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/b460afbb-ff54-4f1d-bc25-3d7ed35a05d4)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/32f3ed62-cc87-435e-a9ed-ab0cf84704f9)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/99074e9f-7e6e-4f4c-a2bb-a913445160a7)

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
 ![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/b07f2eba-3621-42e6-8768-75f90e2ba524)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/835e868a-8fbc-4b88-ae1b-37d952bc6b0c)
 
 
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
$chmod 755 forin1.sh
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/d4152b60-7d43-4105-b4c6-b925819ed38e)

 
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
 ![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/5491ec87-ed3a-45f3-ad66-00934d036417)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/4e5c255e-9230-4784-abdf-21836ce03518)
 
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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/43ed8f01-30e0-44ff-a985-0423586d1824)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/25c228e4-26f0-4d49-89ae-c2d360ec25a9)


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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/07640af5-c9db-4c20-a4f3-5e02e71440ac)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/8e79819c-df34-4ef3-b155-37accf107348)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/4b0bae98-dfc8-4ee4-9c10-afa5d4722f55)

 
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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/3d29e097-1d46-4933-b13d-1ad62a0ab0b9)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 ![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/bd3dff4e-8617-42d9-a083-e06db21be436)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/1cbee726-1940-4e07-90e9-c6822a283882)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 





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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/a7c26e7e-6433-468c-a903-aa928e3fd75e)

 
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


$ ./argshift.sh 1 2 3
## OUTPUT
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/44f1a951-cc2c-4139-a32f-c4f0c0bf8f62)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/c2d2b114-d5ec-47e0-a6f9-b22b73dce2ca)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/5a54e2b5-cb4c-4d1c-8300-6e92ec82e212)

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
 ![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/be026c21-09da-4fe3-9557-6bce7b8a6e0e)

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
![image](https://github.com/SGokul2005/OS-Linux-commands-Shell-script/assets/147121825/a9f4e7e1-37a7-4a86-b229-96da0dc46813)


# RESULT:
The Commands are executed successfully.
