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
![WhatsApp Image 2024-09-19 at 8 22 09 AM(10)](https://github.com/user-attachments/assets/250f04c8-7b85-486d-8a97-0ca66d5a5afb)



cat < file2
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 22 09 AM(11)](https://github.com/user-attachments/assets/cb628c79-92cb-4f47-96f5-cf88279174dc)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![WhatsApp Image 2024-09-19 at 8 28 12 AM(2)](https://github.com/user-attachments/assets/3ec79294-c003-49a3-99c2-60fbf0d2cf5b)

comm file1 file2
 ## OUTPUT
 ![WhatsApp Image 2024-09-19 at 8 22 09 AM(9)](https://github.com/user-attachments/assets/9ca9c7c1-3ff9-430f-989e-ee61d5935c08)


 
diff file1 file2
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 11 AM(1)](https://github.com/user-attachments/assets/9f294468-57ad-40dd-9ef9-2cf1ec56b2ba)


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

![WhatsApp Image 2024-09-19 at 8 29 06 AM(48)](https://github.com/user-attachments/assets/a47e0c55-a760-4cea-ba9e-d9896bf04f16)



cut -d "|" -f 1 file22
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(48)](https://github.com/user-attachments/assets/7c3f7be9-fed6-4d86-8a0a-b673a963b829)


cut -d "|" -f 2 file22
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(50)](https://github.com/user-attachments/assets/8b20b38b-4978-49c7-86a2-f483eb1f8bcd)


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

![WhatsApp Image 2024-09-19 at 8 29 06 AM(51)](https://github.com/user-attachments/assets/dd06f17c-d684-4452-afdb-be3e391af133)


grep hello newfile 
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/ca2439bc-24b4-4581-9221-74fa0c59eab0)



grep -v hello newfile 
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(50)](https://github.com/user-attachments/assets/ace8fd1c-c9a0-47f6-a659-a4eec0db7af2)



cat newfile | grep -i "hello"
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(53)](https://github.com/user-attachments/assets/28f6cd7d-3660-4f85-b0cc-031278f14f1e)



cat newfile | grep -i -c "hello"
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/d3f9b41a-aad8-4492-bc8c-60718bffea6a)



grep -R ubuntu /etc
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(53)](https://github.com/user-attachments/assets/d736db75-90fd-410e-95b3-725e34d7fa92)


grep -w -n world newfile   
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/ce248cdd-3080-4159-8554-54f600af2fbe)


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

![WhatsApp Image 2024-09-19 at 8 29 06 AM(53)](https://github.com/user-attachments/assets/9c323b17-520f-40de-a349-fbc4939435ce)


egrep -w '(H|h)ello' newfile 
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/7b4e9864-4732-4def-8295-f23cf75ed2c9)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(53)](https://github.com/user-attachments/assets/3e320971-6db9-4642-9e7d-ed0b0f3e3ac6)




egrep '(^hello)' newfile 
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/2ef93cbf-2f22-4e36-98ec-a6beb82a3ab8)



egrep '(world$)' newfile 
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(53)](https://github.com/user-attachments/assets/4a9ba85d-c29e-4970-89d1-a523fbec8a66)


egrep '(World$)' newfile 
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/7045a6d0-b787-4c12-8b98-8b51657d9f07)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/9c4349b5-4ba5-42df-93ca-159345141c1d)


egrep '[1-9]' newfile 
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/2f9c867e-249a-4e2c-ae68-7451ddb2be28)



egrep 'Linux.*world' newfile 
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/39fa9a4e-3c3c-48ce-9e62-ae0f5e42e62b)


egrep 'Linux.*World' newfile 
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/f96d4b5b-1008-44fe-83b1-f039dddefdb5)


egrep l{2} newfile
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/95676e9c-5441-42a4-9abb-7217249aae4a)


egrep 's{1,2}' newfile
## OUTPUT 
![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/259d656c-72ea-459b-abf3-f6461890a5a8)


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

![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/9ea6ed8c-5ff1-4104-9860-1991c85ce2af)


sed -n -e '$p' file23
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/41cd04f4-6e27-4fda-a770-2c1ca85c96a0)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(52)](https://github.com/user-attachments/assets/f2b0b427-347d-4349-932e-4ec780b29d0c)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/bbccc3c0-3f45-45ec-b363-6261ab7d07d2)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(55)](https://github.com/user-attachments/assets/57474da9-bf00-46a5-a503-4019b7dbb459)



sed -n -e '1,5p' file23
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/0a994b2c-ba3d-4309-8cae-7f196bae82c4)


sed -n -e '2,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(56)](https://github.com/user-attachments/assets/6a2b4f25-6e46-4266-a0e0-ba505b92cf39)



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/79f963b4-b795-43b6-80cf-2c237261215c)


seq 10 
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(55)](https://github.com/user-attachments/assets/d21f6434-f853-4ba5-adf1-848e221f76ad)



seq 10 | sed -n '4,6p'
## OUTPUT

![Screenshot 2024-09-21 125127](https://github.com/user-attachments/assets/8ff4a5b5-aca9-4a2d-8b5c-0ea8ce35826e)


seq 10 | sed -n '2,~4p'
## OUTPUT

![Screenshot 2024-09-21 125325](https://github.com/user-attachments/assets/fe27458f-c8cc-449b-aaa4-45b8d4e9ab42)


seq 3 | sed '2a hello'
## OUTPUT

![Screenshot 2024-09-21 125405](https://github.com/user-attachments/assets/1900a625-8d5e-4e29-a644-a856de5fd34d)


seq 2 | sed '2i hello'
## OUTPUT

![Screenshot 2024-09-21 125529](https://github.com/user-attachments/assets/e7d8d854-28af-4f32-b677-3b913bbb2066)

seq 10 | sed '2,9c hello'
## OUTPUT

![Screenshot 2024-09-21 125907](https://github.com/user-attachments/assets/1a841440-eb92-409d-96e1-b3a350b13b2e)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![Screenshot 2024-09-21 125704](https://github.com/user-attachments/assets/8b1ecd7c-4844-4f7a-99f1-5a40f4f1d0be)

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
![Screenshot 2024-09-21 130225](https://github.com/user-attachments/assets/5cbdb8b2-5591-4eb9-8923-b45153b40abd)


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

![Screenshot 2024-09-21 130140](https://github.com/user-attachments/assets/203482ac-e48e-43a9-9838-77dcef11390b)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2024-09-21 130140](https://github.com/user-attachments/assets/cd6b7cf0-5ecd-46d8-8a36-816f9890b84f)

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

![WhatsApp Image 2024-09-19 at 8 28 12 AM(2)](https://github.com/user-attachments/assets/996acd25-7913-4ab8-8f6a-5dabe92188e2)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 28 12 AM(7)](https://github.com/user-attachments/assets/93116f8a-4d23-4c69-8cea-3e7aed80d30f)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 28 12 AM(2)](https://github.com/user-attachments/assets/f739162d-b7ea-429b-b1eb-6a6856f17149)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/379e231d-e515-4a08-9f2b-9516d64bb765)

tar -xvf backup.tar
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(56)](https://github.com/user-attachments/assets/b4a15070-1a2c-465a-9ab6-947144596688)

gzip backup.tar

ls .gz
## OUTPUT
 ![WhatsApp Image 2024-09-19 at 8 29 06 AM(54)](https://github.com/user-attachments/assets/4de988b6-74e2-42ab-9b6e-b25609e1615f)

gunzip backup.tar.gz
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 29 06 AM(56)](https://github.com/user-attachments/assets/356a66c5-a3c0-436f-9152-46e4f9f1d3b6)

 
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

![WhatsApp Image 2024-09-19 at 8 19 24 AM(2)](https://github.com/user-attachments/assets/89276863-f103-4911-a21a-7dac3a01b35b)

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
![WhatsApp Image 2024-09-19 at 8 20 03 AM(1)](https://github.com/user-attachments/assets/ac5d51cb-7339-4c3a-97d4-4e79cebe5aa7)

 
ls file1
## OUTPUT
![WhatsApp Image 2024-09-19 at 8 22 10 AM(5)](https://github.com/user-attachments/assets/a86192f4-af2f-4915-be7d-34abc227e018)

echo $?
## OUTPUT 
![WhatsApp Image 2024-09-19 at 8 22 10 AM(6)](https://github.com/user-attachments/assets/e82cca71-5a9e-43ee-a925-d8d624f99c37)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![WhatsApp Image 2024-09-19 at 8 22 10 AM(6)](https://github.com/user-attachments/assets/668ef701-1caf-4db2-82af-bf7d1ce0b544)

abcd
 
echo $?
 ## OUTPUT


 ![WhatsApp Image 2024-09-19 at 8 22 10 AM(6)](https://github.com/user-attachments/assets/198c33e0-87a7-4264-ae2c-914b5991e62c)

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

![WhatsApp Image 2024-09-19 at 8 22 10 AM(5)](https://github.com/user-attachments/assets/cb392eee-d05c-4e56-be22-4dacba845f63)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2024-09-19 09-35-19](https://github.com/user-attachments/assets/10e14d5f-19cb-4e3d-b6cc-8382a4f2410f)



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
![Screenshot from 2024-09-19 09-36-11](https://github.com/user-attachments/assets/180fac29-20c2-49c8-bed2-6de0893603aa)


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
![Screenshot from 2024-09-19 09-36-51](https://github.com/user-attachments/assets/98ee1ae6-64e2-408d-9300-587ef7ac1db2)



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
![Screenshot from 2024-09-19 09-37-37](https://github.com/user-attachments/assets/be60af4d-43cd-442a-b48f-f2b9b7fc19e5)

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
![Screenshot from 2024-09-19 09-38-24](https://github.com/user-attachments/assets/2d632d02-e148-496b-bf99-97292fd2e83d)

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
![Screenshot from 2024-09-19 09-39-17](https://github.com/user-attachments/assets/d25a2e2c-2df2-42b5-8f1a-c4679f66ba72)


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
![Screenshot from 2024-09-19 09-39-53](https://github.com/user-attachments/assets/e64bf029-76ad-4977-b8af-99d6c4af08ac)

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
![Screenshot from 2024-09-19 09-40-34](https://github.com/user-attachments/assets/eb3ab61b-7b6d-4a2b-9c28-16eb91fc4aa3)

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
![Screenshot from 2024-09-19 09-41-13](https://github.com/user-attachments/assets/071f3cdf-08ef-4e86-8f46-e06b3ce49a56)


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


![Screenshot from 2024-09-19 09-42-42](https://github.com/user-attachments/assets/e56cbf98-97aa-42fd-b81d-92a9bd4d0ea2)

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
![Screenshot from 2024-09-19 09-41-49](https://github.com/user-attachments/assets/121c0bd2-a4a2-47e9-9f9d-4809e31d7a49)

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

![Screenshot from 2024-09-19 09-43-32](https://github.com/user-attachments/assets/9a8c9519-4b31-488a-b34c-8e71f8de5db5)

 
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


![Screenshot from 2024-09-19 09-44-12](https://github.com/user-attachments/assets/7467ce24-8b78-4eba-a87f-ea78e8b6b7c8)



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

![image](https://github.com/user-attachments/assets/d0682945-664b-471e-8eb2-c1b1647a2c4a)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![image](https://github.com/user-attachments/assets/fe8ef2d5-cc88-4270-bf7c-c0a1896660ab)



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

![Screenshot from 2024-09-19 09-46-08](https://github.com/user-attachments/assets/1eb4b926-263d-49c3-a1b1-583b7eba87bd)

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

![Screenshot from 2024-09-19 09-47-54](https://github.com/user-attachments/assets/b60da60d-4913-4a40-af50-92a81e8ec024)

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

![Screenshot from 2024-09-19 09-49-27](https://github.com/user-attachments/assets/5addcd01-b352-434f-b687-84581112dfd3)

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

![Screenshot from 2024-09-19 09-49-57](https://github.com/user-attachments/assets/3ce9829a-e504-49e3-8d49-44decf5049f8)


# RESULT:
The Commands are executed successfully.
