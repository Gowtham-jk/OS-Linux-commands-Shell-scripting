# OS-Linux-commands-Shell-scripting
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
![Screenshot 2024-02-28 214631](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/91d721d5-8737-4df9-9cf0-7cbcdca530f4)


cat < file2
## OUTPUT
![Screenshot 2024-02-28 214641](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/563c88e8-e081-4588-b4c2-146314f46e6b)


# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot 2024-02-28 214649](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/a25f6422-8212-4acd-bc5c-88c7544cf980)


comm file1 file2
 ## OUTPUT
![Screenshot 2024-02-28 214657](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/976c6db4-14e0-444d-b2ac-40bd38dda1e9)


 
diff file1 file2
## OUTPUT
![Screenshot 2024-02-28 214705](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/593b5403-83c2-4bd1-89a6-a254f22ee720)



#Filters

### Create the following files file11, file22 as follows:

cut -c1-3 file11
## OUTPUT

![Screenshot 2024-02-28 214713](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/4061802a-5588-4196-8b26-c6cc05374962)


cut -d "|" -f 1 file22
## OUTPUT
![Screenshot 2024-02-28 214718](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/f0bf780f-ef51-4c58-ba0c-e5e300edccce)


cut -d "|" -f 2 file22
## OUTPUT
cat < newfile 
![Screenshot 2024-02-28 214725](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/32aa2c21-b191-4bd7-98c3-ccbdc98ec820)


## OUTPUT
![Screenshot 2024-02-28 214732](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/7ce08ef8-83cf-42b6-9f00-5fe7774dc942)


grep hello newfile 
## OUTPUT
![Screenshot 2024-02-28 214737](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/cd46ea62-a81f-40b0-8629-b51e3a1872ce)


grep -v hello newfile 
## OUTPUT
![Screenshot 2024-02-28 214747](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/a5e80d6e-321e-49b0-b11a-47fd44c9ccaf)


cat newfile | grep -i "hello"
## OUTPUT
![Screenshot 2024-02-28 214754](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/1195e91a-89f7-4283-bc2d-7f79fc70089c)


cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot 2024-02-28 214800](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/99c62be9-e327-44e5-bf0e-d443fb3a2fe4)

grep -R ubuntu /etc
## OUTPUT
![Screenshot 2024-02-28 214806](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/e36e3ebf-0714-4eb4-848f-8ffb61fca0fb)


grep -w -n world newfile   
## OUTPUT
![Screenshot 2024-02-28 214813](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/d4e26160-829f-40d9-94c4-c89f717c1ae7)

egrep -w 'Hello|hello' newfile 
## OUTPUT
![Screenshot 2024-02-28 214820](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/5001954c-b951-47d4-bf0f-b9257ad78d72)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot 2024-02-28 214826](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/930ef512-a060-4ecc-ad2e-05bde75a0c81)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot 2024-02-28 214831](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/db0e9a95-9eaa-4505-899a-d7a88ba1cead)


egrep '(^hello)' newfile 
## OUTPUT
![Screenshot 2024-02-28 214837](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/190f2625-121f-4292-9649-58372f609bb8)


egrep '(world$)' newfile 
## OUTPUT
![Screenshot 2024-02-28 214843](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/4595b287-6847-4cdc-acfb-2f3cddca6eb8)


egrep '(World$)' newfile 
## OUTPUT
![Screenshot 2024-02-28 214849](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/dd0a52cc-34d4-459b-bce9-975f4ff499d2)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot 2024-02-28 214855](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/8938329e-7857-405e-b85a-9dd77ca9082c)

egrep '[1-9]' newfile 
## OUTPUT
![Screenshot 2024-02-28 214907](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/b07df532-a7ef-45db-9ad7-9eb8efa6dac8)


egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot 2024-02-28 214919](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/db8b38d6-62f8-4ac6-85d8-257f8294813a)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/deepika3095/OS-Linux-commands-Shell-script/assets/151625159/57a931c1-b4a9-474b-85f6-673a6677fa74)

egrep l{2} newfile
## OUTPUT
![image](https://github.com/deepika3095/OS-Linux-commands-Shell-script/assets/151625159/0b0e3818-ad4a-4457-8d48-bb0b9781d525)

## OUTPUT 


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

![Screenshot 2024-02-28 215932](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/aa57338f-f308-4af3-9396-6f70dbd4f46c)

sed -n -e '3p' file23
## OUTPUT
![Screenshot 2024-02-28 220016](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/7ef2c7a2-55ce-49cb-92de-8b00ed2b8d3a)


sed -n -e '$p' file23
## OUTPUT
![Screenshot 2024-02-28 220023](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/2f07748f-5b22-47ce-be71-902a3db801dc)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-02-28 220030](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/4f92160f-9300-4b4f-9fb7-c871f0df6880)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot 2024-02-28 220036](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/e9c8bd70-0f0c-4f0f-b161-64fa2da4bbd3)

sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot 2024-02-28 220045](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/7028f8f0-bafb-4efb-8c40-26d3aab04563)

sed -n -e '1,5p' file23
## OUTPUT
![Screenshot 2024-02-28 220052](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/3f7ca4bc-fad1-4229-ae46-70c9dbb5fc15)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot 2024-02-28 220057](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/c457c091-f21e-4a53-bf29-e2dd645a9fc5)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot 2024-02-28 220102](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/c29d3fde-9bd5-458d-bc24-164a6193a1a8)


seq 10 
## OUTPUT
![Screenshot 2024-02-28 220107](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/f698533e-9215-43ed-9d52-6e10aacc79e6)

seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot 2024-02-28 220112](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/5670977a-af81-4098-a209-66a4e60c232b)


seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot 2024-02-28 220120](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/6ca57a97-d17e-48a0-b381-87324a43d1d1)


seq 3 | sed '2a hello'
## OUTPUT
![Screenshot 2024-02-28 220126](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/0e0bb131-3fbd-483a-9325-7653703fab2d)


seq 2 | sed '2i hello'
## OUTPUT
![Screenshot 2024-02-28 220134](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/64d21a59-7bf7-4cfc-ba9d-62c06d68eab2)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot 2024-02-28 220140](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/dc0b7447-cfad-40b7-b8da-f68809cf9d52)


## OUTPUT
![Screenshot 2024-02-28 220147](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/737afdd6-bbcf-4864-a164-6cb7495e612e)

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
![Screenshot 2024-02-28 220456](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/192b9ff6-eaab-4793-80b8-7068c3f239b2)


## OUTPUT
![Screenshot 2024-02-28 220502](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/905d9a85-95bb-4374-87ed-29ddedc6c425)


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
![Screenshot 2024-02-28 220509](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/634c199d-f830-43b2-a2e2-63897cce3507)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot 2024-02-28 220516](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/eeb303f6-6aa5-4392-8e84-59abefa9b877)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```

```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![Screenshot 2024-02-28 220522](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/d90786bd-bba9-4e12-9f86-bad56e9141d0)


cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot 2024-02-28 220528](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/67735b04-5405-453d-8ca2-0fd18e902a02)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![Screenshot 2024-02-28 220534](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/48e6366b-18d2-400e-8419-c87c240fc7a4)

mkdir backupdir
mv backup.tar backupdir 
tar -tvf backup.tar
## OUTPUT
![Screenshot 2024-02-28 220539](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/69f65b0a-b3c1-406f-aa69-2a97ea517a08)


tar -xvf backup.tar

## OUTPUT
![Screenshot 2024-02-28 220545](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/6ddbe653-d65e-4b6b-9ce6-854609e59e4e)


# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot 2024-02-28 220830](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/58489cdf-5a2f-4119-a5a2-db3b0f35a3b6)


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![Screenshot 2024-02-28 220837](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/ed8d1f2a-50f6-4df4-a2fa-6a30f52affe8)


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
![Screenshot 2024-02-28 220842](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/f8e51f27-4ef5-451c-a0ea-c7aa88e9621a)

echo $?
## OUTPUT 
![Screenshot 2024-02-28 220847](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/09b399ea-adb3-4412-bd4f-9ca852c7e55a)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![Screenshot 2024-02-28 220856](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/47965d67-41a2-467d-9570-86a2893b16ad)


abcd
 
echo $?

 
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
![Screenshot 2024-02-28 220901](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/df59146e-721e-4791-8b26-f51bae4ef848)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot 2024-02-28 220906](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/a73e36ba-68d7-495c-b933-999923c12f04)


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
![Screenshot 2024-02-28 220912](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/d8035e61-7145-486d-ac6e-aa8e0adf1820)


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

![Screenshot 2024-02-28 220918](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/6885c335-399d-4f26-a9ca-1dac7810b271)


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



vi

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT

![Screenshot 2024-02-28 220924](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/e0a0177d-f7f3-4653-87f0-804077b28d7d)


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

![Screenshot 2024-02-28 220935](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/88313dcf-c200-468b-8040-19d7ab02bee8)


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
![Screenshot 2024-02-28 220941](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/ba6386e1-1215-4315-96dd-9e5af10f748d)



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

![Screenshot 2024-02-28 220948](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/b1c303c6-a587-4382-9656-2fea15b5feba)


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
 ## Output
 
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
 
  ## Output

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
 
 
 ## Output
![Screenshot 2024-02-28 220954](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/edc2a157-8f90-4d3e-b2b8-2e8a4bef238c)

 

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
 
 ## Output
![Screenshot 2024-02-28 220959](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/e2c61b09-7ebb-461e-a6d3-87f9ddb062a9)

 
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
## Output

![Screenshot 2024-02-28 221004](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/f2574164-0a85-4db4-8e24-3a18f4941205)


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
  ## Output
![Screenshot 2024-02-28 221012](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/57993696-75ed-4eca-ad23-042823db777b)


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
  ## Output

![Screenshot 2024-02-28 221018](https://github.com/Gowtham-jk/OS-Linux-commands-Shell-scripting/assets/149857834/f128f66b-3272-47f2-803b-7da7e50353cc)


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
file ="cities"
for state in 'cat $file'
do
echo "Visit beautiful $file"
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
