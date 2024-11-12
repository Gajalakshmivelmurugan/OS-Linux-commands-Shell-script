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
![368828139-250f04c8-7b85-486d-8a97-0ca66d5a5afb](https://github.com/user-attachments/assets/6bb27e39-9036-4ced-a2e9-7ec8db38b0f9)

cat < file2
## OUTPUT
![368828346-cb628c79-92cb-4f47-96f5-cf88279174dc](https://github.com/user-attachments/assets/c5bc18f4-97b4-4a08-9509-2e934f494f5b)

# Comparing Files
cmp file1 file2
## OUTPUT
![368828740-3ec79294-c003-49a3-99c2-60fbf0d2cf5b](https://github.com/user-attachments/assets/4aaa5c3e-47e7-4c59-b90d-07f57d8e02bc)

comm file1 file2
 ## OUTPUT
 ![368828911-9ca9c7c1-3ff9-430f-989e-ee61d5935c08](https://github.com/user-attachments/assets/ffe7c8c9-7c25-4f63-9d39-b8f303fe4d3a)

diff file1 file2
## OUTPUT
![368829529-9f294468-57ad-40dd-9ef9-2cf1ec56b2ba](https://github.com/user-attachments/assets/3d42fc87-cd42-4ee0-8a48-c1dd1fe892c4)


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
![368830067-a47e0c55-a760-4cea-ba9e-d9896bf04f16](https://github.com/user-attachments/assets/f1f3cd9d-4038-478d-82b8-9573e2f464d3)

cut -d "|" -f 1 file22
## OUTPUT
![368830131-7c3f7be9-fed6-4d86-8a0a-b673a963b829](https://github.com/user-attachments/assets/fc4c2164-cff8-4fc1-afce-cc3f8c7df948)

cut -d "|" -f 2 file22
## OUTPUT
![368830453-8b20b38b-4978-49c7-86a2-f483eb1f8bcd](https://github.com/user-attachments/assets/9e8c8b72-f242-44ac-9b7f-ccfa61400909)

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
![368830664-dd06f17c-d684-4452-afdb-be3e391af133](https://github.com/user-attachments/assets/1dd7c757-8536-41e4-9da7-a817536e17b8)

grep hello newfile 
## OUTPUT
![368830848-ca2439bc-24b4-4581-9221-74fa0c59eab0](https://github.com/user-attachments/assets/2f2c2939-f63f-4f44-9b90-703fe8b29ccd)

grep -v hello newfile 
## OUTPUT
![368830771-ace8fd1c-c9a0-47f6-a659-a4eec0db7af2](https://github.com/user-attachments/assets/97481d9a-8699-4ae9-8f96-4cc6c64d0f87)

cat newfile | grep -i "hello"
## OUTPUT
![368830934-28f6cd7d-3660-4f85-b0cc-031278f14f1e](https://github.com/user-attachments/assets/cc675766-b3a1-4ab5-9351-ff87f360c811)

cat newfile | grep -i -c "hello"
## OUTPUT
![368831020-d3f9b41a-aad8-4492-bc8c-60718bffea6a](https://github.com/user-attachments/assets/c2a69602-b5d4-4e55-85c6-9baf93e50e83)

grep -R ubuntu /etc
## OUTPUT
![368831116-d736db75-90fd-410e-95b3-725e34d7fa92](https://github.com/user-attachments/assets/f18a5b7b-e939-4aa5-aba5-84c76a911b04)

grep -w -n world newfile   
## OUTPUT
![368831197-ce248cdd-3080-4159-8554-54f600af2fbe](https://github.com/user-attachments/assets/10724af6-aac4-4820-8932-487d7f7a374b)

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
![368831283-9c323b17-520f-40de-a349-fbc4939435ce](https://github.com/user-attachments/assets/26a47774-dde7-4803-b687-90acbd96954c)

egrep -w '(H|h)ello' newfile 
## OUTPUT
![368831349-7b4e9864-4732-4def-8295-f23cf75ed2c9](https://github.com/user-attachments/assets/57049730-786a-4483-9291-dd088dad86ed)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![368831416-3e320971-6db9-4642-9e7d-ed0b0f3e3ac6](https://github.com/user-attachments/assets/2d385f34-7c31-4d57-9c68-62a3ada1331f)

egrep '(^hello)' newfile 
## OUTPUT
![368831526-2ef93cbf-2f22-4e36-98ec-a6beb82a3ab8](https://github.com/user-attachments/assets/dfb441af-b2d8-4612-822a-8d3fd1905309)

egrep '(world$)' newfile 
## OUTPUT
![368831599-4a9ba85d-c29e-4970-89d1-a523fbec8a66](https://github.com/user-attachments/assets/c5a30e24-9ca6-4951-bbcf-2e397bf998d9)

egrep '(World$)' newfile 
## OUTPUT
![368831746-7045a6d0-b787-4c12-8b98-8b51657d9f07](https://github.com/user-attachments/assets/cdc51445-8eeb-482b-83de-ecbdbd8ecfb2)

egrep '((W|w)orld$)' newfile 
## OUTPUT
![368831807-9c4349b5-4ba5-42df-93ca-159345141c1d](https://github.com/user-attachments/assets/ca90ddca-915c-4ab8-9033-f1e9bb9cbe6b)

egrep '[1-9]' newfile 
## OUTPUT
![368831878-2f9c867e-249a-4e2c-ae68-7451ddb2be28](https://github.com/user-attachments/assets/92ca8a0a-ec04-4ea5-9d16-576a7cde99fb)

egrep 'Linux.*world' newfile 
## OUTPUT
![368831936-39fa9a4e-3c3c-48ce-9e62-ae0f5e42e62b](https://github.com/user-attachments/assets/eab09e94-af87-4a32-98ea-5e1e8bfa9302)

egrep 'Linux.*World' newfile 
## OUTPUT
![368832007-f96d4b5b-1008-44fe-83b1-f039dddefdb5](https://github.com/user-attachments/assets/4846662e-0957-48cc-a7b1-98c05c2a58cc)

egrep l{2} newfile
## OUTPUT
![368832075-95676e9c-5441-42a4-9abb-7217249aae4a](https://github.com/user-attachments/assets/3b734a37-78c5-40f8-ab98-9bcecbd1536d)

egrep 's{1,2}' newfile
## OUTPUT 
![368832140-259d656c-72ea-459b-abf3-f6461890a5a8](https://github.com/user-attachments/assets/aece3ed9-67b6-4984-8bc5-eb3bba811390)

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
![368832258-9ea6ed8c-5ff1-4104-9860-1991c85ce2af](https://github.com/user-attachments/assets/7798aec0-ec44-43cf-94c0-613990bc90fe)

sed -n -e '$p' file23
## OUTPUT
![368832328-41cd04f4-6e27-4fda-a770-2c1ca85c96a0](https://github.com/user-attachments/assets/d5472b4a-f081-4b62-b98f-da6720aba01a)

sed  -e 's/Ram/Sita/' file23
## OUTPUT
![368832451-f2b0b427-347d-4349-932e-4ec780b29d0c](https://github.com/user-attachments/assets/565607bc-32c7-4131-b0df-0b0fe88830ff)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![368832523-bbccc3c0-3f45-45ec-b363-6261ab7d07d2](https://github.com/user-attachments/assets/1ce34dd4-fb73-48a8-8bf5-82f79708ceaf)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![368832591-57474da9-bf00-46a5-a503-4019b7dbb459](https://github.com/user-attachments/assets/29e9e620-6955-4ef4-8b7f-205353b1e8db)

sed -n -e '1,5p' file23
## OUTPUT
![368832734-0a994b2c-ba3d-4309-8cae-7f196bae82c4](https://github.com/user-attachments/assets/19a582ee-f8cb-4339-8539-4959ae7cf3a4)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![368832799-6a2b4f25-6e46-4266-a0e0-ba505b92cf39](https://github.com/user-attachments/assets/d776521f-34e2-4902-b41f-5abdb02538df)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![368832882-79f963b4-b795-43b6-80cf-2c237261215c](https://github.com/user-attachments/assets/9450290a-28fd-4167-9b39-be6b21dac784)

seq 10 
## OUTPUT
![368833046-d21f6434-f853-4ba5-adf1-848e221f76ad](https://github.com/user-attachments/assets/4ade691a-859b-4f8e-be13-db700f24a6c6)

seq 10 | sed -n '4,6p'
## OUTPUT
![369619374-8ff4a5b5-aca9-4a2d-8b5c-0ea8ce35826e](https://github.com/user-attachments/assets/7216489e-b62f-4581-b371-6a856e18c94d)

seq 10 | sed -n '2,~4p'
## OUTPUT
![369619421-fe27458f-c8cc-449b-aaa4-45b8d4e9ab42](https://github.com/user-attachments/assets/a3d5dea9-4ddd-4b10-8937-cb1a3b323792)

seq 3 | sed '2a hello'
## OUTPUT
![369619448-1900a625-8d5e-4e29-a644-a856de5fd34d](https://github.com/user-attachments/assets/d3ed6126-c888-47a3-81fe-cbb5bd9a88c2)

seq 2 | sed '2i hello'
## OUTPUT
![369619521-e7d8d854-28af-4f32-b677-3b913bbb2066](https://github.com/user-attachments/assets/1f2e470f-9680-47fc-9901-dc228c4978be)

seq 10 | sed '2,9c hello'
## OUTPUT
![369619731-1a841440-eb92-409d-96e1-b3a350b13b2e](https://github.com/user-attachments/assets/3c515cd3-da26-4080-94b6-0148bb7da6bb)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![369619637-8b1ecd7c-4844-4f7a-99f1-5a40f4f1d0be](https://github.com/user-attachments/assets/4e225ac7-3cff-40ec-b350-098b10015240)

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
![369619917-5cbdb8b2-5591-4eb9-8923-b45153b40abd](https://github.com/user-attachments/assets/dac85463-5b66-4310-8cf3-bb7cbb32a175)

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
![369619885-203482ac-e48e-43a9-9838-77dcef11390b](https://github.com/user-attachments/assets/da6ffcb6-d5af-473e-8dd1-158a0e97b801)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![369619975-cd6b7cf0-5ecd-46d8-8a36-816f9890b84f](https://github.com/user-attachments/assets/5e57972b-98f6-4732-9067-ad48a9aa0476)

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
![368833852-996acd25-7913-4ab8-8f6a-5dabe92188e2](https://github.com/user-attachments/assets/da479ee0-3662-41e9-9294-9532f3d74a5b)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![368833908-93116f8a-4d23-4c69-8cea-3e7aed80d30f](https://github.com/user-attachments/assets/777ec103-d51d-42ab-8d31-76c74b9272b9)

#Backup commands
tar -cvf backup.tar *
## OUTPUT
![368833984-f739162d-b7ea-429b-b1eb-6a6856f17149](https://github.com/user-attachments/assets/8269a987-f74f-46af-8043-0c6b41e2e255)

mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![368834182-379e231d-e515-4a08-9f2b-9516d64bb765](https://github.com/user-attachments/assets/f63b0747-f882-4359-9e1a-ac92fa83c6c8)

tar -xvf backup.tar
## OUTPUT
![368834105-b4a15070-1a2c-465a-9ab6-947144596688](https://github.com/user-attachments/assets/ce1a8fd4-ebb4-4a26-a353-02042a144ece)

gzip backup.tar

ls .gz
## OUTPUT
![368834052-4de988b6-74e2-42ab-9b6e-b25609e1615f](https://github.com/user-attachments/assets/2f955093-4905-4a0d-8ee0-a12ac8da71fb)

gunzip backup.tar.gz
## OUTPUT
![368834247-356a66c5-a3c0-436f-9152-46e4f9f1d3b6](https://github.com/user-attachments/assets/1881e9c1-88f7-4786-be8e-7292a4941c55)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh

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
![368834716-89276863-f103-4911-a21a-7dac3a01b35b](https://github.com/user-attachments/assets/89fd1982-018a-4291-abba-0b71fc650b0f)

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
![368834808-ac5d51cb-7339-4c3a-97d4-4e79cebe5aa7](https://github.com/user-attachments/assets/74442991-eba7-45af-bfa2-af04bdd7dd99)

ls file1
## OUTPUT
![368834918-a86192f4-af2f-4915-be7d-34abc227e018](https://github.com/user-attachments/assets/d19af752-55f9-4b13-85b8-771a615f73b6)

echo $?
## OUTPUT 
./one bash: ./one: Permission denied
 echo $?
## OUTPUT 
 ![368835082-668ef701-1caf-4db2-82af-bf7d1ce0b544](https://github.com/user-attachments/assets/7929818d-84e3-4146-99ed-acd3d1d08900)

abcd
echo $?
 ## OUTPUT
![368835068-198c33e0-87a7-4264-ae2c-914b5991e62c](https://github.com/user-attachments/assets/20819ab6-9b45-4e16-94b2-b5b80b6d5cf5)

 
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
![368835164-cb392eee-d05c-4e56-be22-4dacba845f63](https://github.com/user-attachments/assets/d71a7f57-167d-446c-a431-de1b5e83fd47)
chmod 755 strcomp.sh
./strcomp.sh 
## OUTPUT
![368837004-10e14d5f-19cb-4e3d-b6cc-8382a4f2410f](https://github.com/user-attachments/assets/3aaaacb1-260a-4170-a2be-435f6b837832)


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
![368837122-180fac29-20c2-49c8-bed2-6de0893603aa](https://github.com/user-attachments/assets/a8f41774-318d-4c07-9049-8b02d8c0199a)

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
![368837241-98ee1ae6-64e2-408d-9300-587ef7ac1db2](https://github.com/user-attachments/assets/1a83f9ec-33ee-4666-9408-aa676c2e55e5)

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
![368837360-be60af4d-43cd-442a-b48f-f2b9b7fc19e5](https://github.com/user-attachments/assets/5553f06b-a5c0-4d32-b105-00ac85653984)

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
![368837488-2d632d02-e148-496b-bf99-97292fd2e83d](https://github.com/user-attachments/assets/c28bb1cf-57df-4ac4-9640-5046335c89de)

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
![368837671-d25a2e2c-2df2-42b5-8f1a-c4679f66ba72](https://github.com/user-attachments/assets/9dedc88e-8f97-4081-8e54-aaf7b82b5129)

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
![368837772-e64bf029-76ad-4977-b8af-99d6c4af08ac](https://github.com/user-attachments/assets/d7bf90e0-b36f-4c7e-bb54-a8e1c702688d)

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
![368837883-eb3ab61b-7b6d-4a2b-9c28-16eb91fc4aa3](https://github.com/user-attachments/assets/9fc4beea-32a9-420d-b320-eadae2dfde30)

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
![368838010-071f3cdf-08ef-4e86-8f46-e06b3ce49a56](https://github.com/user-attachments/assets/138f293a-7c12-40e2-93fd-14d77e553a31)



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
![368838385-e56cbf98-97aa-42fd-b81d-92a9bd4d0ea2](https://github.com/user-attachments/assets/f8395c51-b718-4c61-94a8-4c66c33a1c79)

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
![368838385-e56cbf98-97aa-42fd-b81d-92a9bd4d0ea2](https://github.com/user-attachments/assets/670258cc-229d-4874-8761-c859e302a14c)

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
![368838162-121c0bd2-a4a2-47e9-9f9d-4809e31d7a49](https://github.com/user-attachments/assets/12e4bccc-5201-4f5f-9757-45a59c131016)

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
![368838496-9a8c9519-4b31-488a-b34c-8e71f8de5db5](https://github.com/user-attachments/assets/34e755e4-6537-4689-8ffd-849e18fe8760)

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
![369620192-50d3ddaa-5611-4c83-a79d-dc5acdd527c7](https://github.com/user-attachments/assets/afe93279-4971-46e3-8583-a8854d41e5a7)

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
![368838806-d0682945-664b-471e-8eb2-c1b1647a2c4a](https://github.com/user-attachments/assets/f1311754-42ca-46e3-8b4b-035e7ba2720f)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![368838876-fe8ef2d5-cc88-4270-bf7c-c0a1896660ab](https://github.com/user-attachments/assets/b59b2e9b-e7d2-446d-a290-66eaeca0c32a)

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
![368839224-1eb4b926-263d-49c3-a1b1-583b7eba87bd](https://github.com/user-attachments/assets/f17360ab-5f47-459f-b6d9-f4f948843fb3)

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
![368839335-b60da60d-4913-4a40-af50-92a81e8ec024](https://github.com/user-attachments/assets/57c2109b-8c19-4f50-8b03-8c57577593ad)

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
![369620230-05daab37-8960-406b-94c3-ec82d02b94cf](https://github.com/user-attachments/assets/bf538ca8-dad7-4c43-ace4-8888d1ac7528)


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
![368839621-5addcd01-b352-434f-b687-84581112dfd3](https://github.com/user-attachments/assets/703483f0-23ab-483a-81ad-e66a85f21b94)

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
![369620270-6e983007-6625-4e0a-90b1-e6a20898374b](https://github.com/user-attachments/assets/3f905203-6f83-413e-bfdb-7bf63c9d7cae)

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
![368839668-3ce9829a-e504-49e3-8d49-44decf5049f8](https://github.com/user-attachments/assets/e2c29d2d-59d3-43b7-ba21-faae8f445eb0)

# RESULT:
The Commands are executed successfully.
