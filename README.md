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



cat < file2
## OUTPUT


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="806" height="81" alt="Screenshot 2026-05-09 180744" src="https://github.com/user-attachments/assets/db181ed3-6ed2-43be-9926-72b66e51d3d4" />

comm file1 file2
 ## OUTPUT
<img width="794" height="222" alt="Screenshot 2026-05-10 124827" src="https://github.com/user-attachments/assets/c4db58bc-ed53-493e-9cf0-d95b01f56f11" />

 
diff file1 file2
## OUTPUT

<img width="800" height="269" alt="Screenshot 2026-05-10 124851" src="https://github.com/user-attachments/assets/1d2128f7-749b-43bd-b0cb-e076c1597410" />

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

<img width="802" height="99" alt="Screenshot 2026-05-10 125100" src="https://github.com/user-attachments/assets/68724968-2967-454e-9638-54bf40b8b5eb" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="959" height="122" alt="Screenshot 2026-05-10 130959" src="https://github.com/user-attachments/assets/acfae1a3-c031-4cef-9aad-6ef9f176868d" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="959" height="121" alt="Screenshot 2026-05-10 131015" src="https://github.com/user-attachments/assets/c4c7c9eb-1aa7-48ad-b533-a364112d0dea" />


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


<img width="809" height="74" alt="Screenshot 2026-05-10 125744" src="https://github.com/user-attachments/assets/5d96fdc8-d43b-4e62-8fc7-6b32f038541c" />

grep hello newfile 
## OUTPUT


<img width="809" height="74" alt="Screenshot 2026-05-10 125744" src="https://github.com/user-attachments/assets/eb31a059-8671-43a7-b375-9e60bb090a65" />



grep -v hello newfile 
## OUTPUT

<img width="810" height="67" alt="Screenshot 2026-05-10 125845" src="https://github.com/user-attachments/assets/19e6d987-7963-417a-ab59-21d3711f1211" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="811" height="97" alt="Screenshot 2026-05-10 125909" src="https://github.com/user-attachments/assets/71cab7b9-7b3b-46bc-b08e-c1b19b4d1f46" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="802" height="73" alt="Screenshot 2026-05-10 130045" src="https://github.com/user-attachments/assets/d6031361-aaa4-41d1-9dba-b7251b67f8d4" />



grep -R ubuntu /etc
## OUTPUT

<img width="950" height="790" alt="Screenshot 2026-05-10 130212" src="https://github.com/user-attachments/assets/5935fa0b-0b80-4d44-85de-e19c223b8b2d" />


grep -w -n world newfile   
## OUTPUT
<img width="958" height="100" alt="Screenshot 2026-05-10 131349" src="https://github.com/user-attachments/assets/7a21b8e0-1358-4748-a9ea-22707b568aa8" />


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

<img width="951" height="92" alt="Screenshot 2026-05-10 131423" src="https://github.com/user-attachments/assets/56763b55-143f-4664-9284-1caf6210dc95" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="921" height="107" alt="Screenshot 2026-05-10 133022" src="https://github.com/user-attachments/assets/08e03294-828e-497f-aadf-9ac5ab2c7f4f" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT



<img width="959" height="94" alt="Screenshot 2026-05-10 131837" src="https://github.com/user-attachments/assets/98e16f8c-b2d6-4340-b0c0-959f88d0c643" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="960" height="74" alt="Screenshot 2026-05-10 131857" src="https://github.com/user-attachments/assets/7e4fd5ff-a1ab-4a18-b617-2480847a72f9" />



egrep '(world$)' newfile 
## OUTPUT

<img width="955" height="97" alt="Screenshot 2026-05-10 131926" src="https://github.com/user-attachments/assets/b5cd908a-f023-474d-9ce4-9195d899387b" />



egrep '(World$)' newfile 
## OUTPUT

<img width="959" height="76" alt="Screenshot 2026-05-10 133033" src="https://github.com/user-attachments/assets/0044d492-a1bd-4530-8447-578a44adaa1c" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="942" height="122" alt="Screenshot 2026-05-10 131946" src="https://github.com/user-attachments/assets/efad0ed4-a5d7-42eb-9864-fa3837ae4de1" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="928" height="72" alt="Screenshot 2026-05-10 132006" src="https://github.com/user-attachments/assets/8faa9fef-6b96-47e8-b5c2-977fc491ea83" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="900" height="75" alt="Screenshot 2026-05-10 132024" src="https://github.com/user-attachments/assets/81ea5b2c-d9bd-46ac-aaea-3fb01893ae0d" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="960" height="72" alt="Screenshot 2026-05-10 132038" src="https://github.com/user-attachments/assets/f9af7954-54eb-436a-a53f-e611050691ed" />


egrep l{2} newfile
## OUTPUT

<img width="961" height="92" alt="Screenshot 2026-05-10 132053" src="https://github.com/user-attachments/assets/ad900011-4970-443c-a183-9e98fa204f52" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="962" height="120" alt="Screenshot 2026-05-10 132128" src="https://github.com/user-attachments/assets/dc023873-ad79-4c19-80e9-5cbc80da4dd1" />


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
<img width="930" height="81" alt="Screenshot 2026-05-10 134406" src="https://github.com/user-attachments/assets/564e4b8a-aeef-4999-9fed-88fc0849d206" />



sed -n -e '$p' file23
## OUTPUT
<img width="957" height="78" alt="Screenshot 2026-05-10 134421" src="https://github.com/user-attachments/assets/c3d353f1-cb3a-44a0-986e-f423b46503e7" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="936" height="251" alt="Screenshot 2026-05-10 134437" src="https://github.com/user-attachments/assets/bdf226b4-a38f-447b-bd62-619e1061b9d4" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="948" height="254" alt="Screenshot 2026-05-10 134515" src="https://github.com/user-attachments/assets/ddd017a0-cc1f-474b-84a8-b2466e3e91bc" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="960" height="249" alt="Screenshot 2026-05-10 134526" src="https://github.com/user-attachments/assets/cafe43f3-bd49-46e6-82af-c1708f2ade2e" />


sed -n -e '1,5p' file23
## OUTPUT


<img width="952" height="179" alt="Screenshot 2026-05-10 134709" src="https://github.com/user-attachments/assets/5bb30dc1-16da-4e2b-bc71-9e99238495bf" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="913" height="124" alt="Screenshot 2026-05-10 134721" src="https://github.com/user-attachments/assets/d3b0e83a-e566-476b-b5e7-b299f0a11a28" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="957" height="104" alt="Screenshot 2026-05-10 134738" src="https://github.com/user-attachments/assets/647559d1-5699-4bb1-97e0-8700c52ac231" />


seq 10 
## OUTPUT

<img width="756" height="298" alt="Screenshot 2026-05-10 135040" src="https://github.com/user-attachments/assets/f5e35368-832e-4e34-8079-d322133f21a1" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="933" height="123" alt="Screenshot 2026-05-10 135102" src="https://github.com/user-attachments/assets/bb5a71d4-4641-4c64-bb14-892934df465f" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="957" height="121" alt="Screenshot 2026-05-10 135115" src="https://github.com/user-attachments/assets/dd960b77-ef31-48d0-bcc1-13b54ef63e71" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="938" height="77" alt="Screenshot 2026-05-10 135134" src="https://github.com/user-attachments/assets/2d45e3af-e7aa-4186-8820-cfd114ebfc67" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="946" height="125" alt="Screenshot 2026-05-10 135158" src="https://github.com/user-attachments/assets/ba40fb0f-3f9e-4176-b171-402550c90d36" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="931" height="119" alt="Screenshot 2026-05-10 135709" src="https://github.com/user-attachments/assets/20f292f3-e894-43dd-830c-f80a2eafd07a" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="959" height="120" alt="Screenshot 2026-05-10 135721" src="https://github.com/user-attachments/assets/ee950bd3-a245-43b8-ad48-96d034b9e710" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="944" height="127" alt="Screenshot 2026-05-10 135734" src="https://github.com/user-attachments/assets/2cb2c6ca-69b9-4fa4-a830-cf9fac42d01e" />



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
