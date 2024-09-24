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
![image](https://github.com/user-attachments/assets/276c7d16-044f-4023-a6b7-07b8513b1482)
cat < file2
## OUTPUT
![image](https://github.com/user-attachments/assets/d52c4027-6300-4110-b241-9be4e6acc68e)
# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/34380661-e366-476f-bd34-a1016672b15a)
comm file1 file2
 ## OUTPUT
![image](https://github.com/user-attachments/assets/c2e364ea-6ce7-4c84-9d61-6dc10cc9c575) 
diff file1 file2
## OUTPUT
![image](https://github.com/user-attachments/assets/26c4a188-87f5-4c48-9a7e-401d288d5f48)
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
![image](https://github.com/user-attachments/assets/ef7f147e-6d4d-4231-adc1-07ac92bc5269)
cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/881ea13b-3d90-4c58-a99a-5d8bb280688b)
cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/user-attachments/assets/3be07d17-6e2d-4896-8ba3-a807549bbed3)
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
![image](https://github.com/user-attachments/assets/0a56501c-5ec4-4b08-8352-ed14e15d59aa)
grep hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ff5a160c-e95a-4d42-8e51-83a96110e725)
grep -v hello newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ad6a2efc-1921-4c29-949c-b4b5da5a6423)
cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/01ff9e06-2985-4c50-8cdd-d3cfc28c1300)
cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/d4f43060-5b4a-4364-aa3b-adf2c47fbec2)
grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/833354f7-5bb0-4f57-ae1b-580110f8e57d)
grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/3db51857-63a1-484a-b82f-911723d6eb16)
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
![image](https://github.com/user-attachments/assets/0b99e7a8-3436-45d0-9b60-a06e0488f65b)
egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/034c2991-cc69-4a67-b072-7dce9cf0650e)
egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f83a8adb-3baf-4df0-94cf-d5a95cc7b597)
egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a4878e89-246c-4ec1-9677-7700b2bff3a6)
egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/adf6fd47-2de6-4a15-98a5-6e67e7790c49)
egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/a9437ea0-fdc4-4c07-bd8c-c45f66d2ebb6)
egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/ac5cf037-0fd0-45bc-8e62-447363129fa1)
egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/46892ad2-8174-45a9-809b-194daabc9a75)
egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/e0603bde-1e1e-43c3-a05b-cf3c4e4c6dc5)
egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/8bc9f1f2-a238-4a29-a14b-a8580a5a003a)
egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/9ada7a39-10db-49ca-b67a-fe6035a1a271)
egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/7ccfdafa-dbbf-4bdf-9328-1182ea0e0de4)
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
![image](https://github.com/user-attachments/assets/59105e53-fd9c-4e5b-8bfd-908eaa922000)
sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/6c53d841-c735-4daf-9225-5f0911bac49f)
sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/cf9c2cad-8010-458f-be84-344420ee750c)
sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/9918fb9b-9549-4473-bfbf-2bfd2e0dd7ef)
sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/17652cf0-1e9c-448d-bfde-12c2707fdcb6)
sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/86ae9bb7-e62d-4cdd-84a2-cf5dc2b7671b)
sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/60c14b92-f44a-463c-9579-b6d5f6d448db)
sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/b767ab59-f507-4ba4-b00a-642b7da61885)
seq 10 
## OUTPUT
seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/62bfbe89-369e-4d2e-bd7b-6cfe496024e2)
seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/525dd887-322d-4b3f-971f-46eb24ed6abe)
seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/68271654-3c35-4444-b1e1-9778f1701fc4)
seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/12eadc5a-83e2-4326-bf82-ca264668c4ee)
seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/641671f7-4ae9-4685-969a-e5f5f1c64d22)
sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/07fcf499-15f0-4191-83cb-06c31292e84c)
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
![image](https://github.com/user-attachments/assets/2435233e-60e7-486a-9f06-343483ffc59d)
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
![image](https://github.com/user-attachments/assets/0ffddd47-75b9-4993-b696-d1d7c95d9769)
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
![image](https://github.com/user-attachments/assets/031bbd61-c986-4aee-a5fa-618d21fc8b39)
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/a1e011c1-9b19-4d3a-bc87-9b23b7374d3e)
#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/98811f62-fe0d-4657-8cb1-bafd35e0e07f)
mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/49302e51-2c6d-4c12-a501-1769f07145d6)
tar -xvf backup.tar
## OUTPUT
![image](https://github.com/user-attachments/assets/08621e88-5aee-4983-b4b1-5e098267518a)
gzip backup.tar

ls .gz
## OUTPUT
![image](https://github.com/user-attachments/assets/7efaaeea-78cc-4548-be90-525cf07539ca)
gunzip backup.tar.gz
## OUTPUT
![image](https://github.com/user-attachments/assets/fb5f8ceb-859b-4599-a54b-a7cf5d68c8a3) 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/user-attachments/assets/497438bc-267a-4dea-86af-486e7c7cc161) 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/b21154a2-e6f3-4d62-b12d-796b51f87256)
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
![image](https://github.com/user-attachments/assets/7323b560-36ef-48ea-bc7d-ea482eef9977) 
ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/bef8fc45-da94-42dd-9484-72bc55602816)
echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
![image](https://github.com/user-attachments/assets/aff878a6-a4f0-456a-bf40-2602ee6cba2b)


 
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
![image](https://github.com/user-attachments/assets/bc5fd499-3b5a-413d-9a4f-2e4c7d85899d)
chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/user-attachments/assets/1c476f66-164d-4a30-84c6-efcec34a8b7c)
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
![image](https://github.com/user-attachments/assets/812dd3de-10f3-4ca2-85d9-f85dd3a8334f)
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
![image](https://github.com/user-attachments/assets/2869e1e9-56f8-4eaf-a14b-ad5a3024ae0c)
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
![image](https://github.com/user-attachments/assets/23df3449-9779-4261-990f-5ebd3fbf53ed)
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
![image](https://github.com/user-attachments/assets/270f0d65-0369-4907-b84e-7bf727d1a86e)
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
![image](https://github.com/user-attachments/assets/373070d5-4c51-410d-848a-c17d190ae69a)
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
![image](https://github.com/user-attachments/assets/12f08e5b-4b53-4387-8a97-cd89bf2e6037)
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
![image](https://github.com/user-attachments/assets/4cb7eb66-72ef-4a1e-9f6f-f6d0d7713f63)
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
![image](https://github.com/user-attachments/assets/f7f43def-2026-4464-81e6-c896bc558da8)
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
![image](https://github.com/user-attachments/assets/992c83d6-516e-4b15-870a-94f195d2837d)
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
![image](https://github.com/user-attachments/assets/b038efe8-37d1-4608-91dd-8f2a635a18d4) 
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
![image](https://github.com/user-attachments/assets/d4bb598c-419e-4cfc-b217-0aab49078f4d)
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
![image](https://github.com/user-attachments/assets/7e3ac9c8-27c5-48f6-ba7f-c939ba7be3ed) 
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
![image](https://github.com/user-attachments/assets/03752a89-d0ef-41b3-8822-68c8e49c1505)
 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/user-attachments/assets/6c73b7bb-9d7f-44e7-b76d-97852d0574f6)
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
![image](https://github.com/user-attachments/assets/45d7b846-446c-4bad-afae-2b4fc7a16251)
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
![image](https://github.com/user-attachments/assets/768ff6f6-b95a-4d38-94f5-372a3f694cf8)

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
![image](https://github.com/user-attachments/assets/be4b29a4-eb85-4c57-a45f-44376f6fc2cd)
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
![image](https://github.com/user-attachments/assets/2d1026bd-7e0f-459d-ae34-38c6335074b5)
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
![image](https://github.com/user-attachments/assets/18f127bc-cf2a-47c2-acb3-c15003e3643d)
# RESULT:
The Commands are executed successfully.
