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
<img width="487" height="117" alt="image" src="https://github.com/user-attachments/assets/5f3dd8cf-971c-4a52-b6ee-11eb11e20615" />




cat < file2
## OUTPUT
<img width="641" height="135" alt="image" src="https://github.com/user-attachments/assets/f2ee7e8e-9053-4afd-a98e-0df2efd77ecc" />



# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="622" height="52" alt="image" src="https://github.com/user-attachments/assets/9169b5f0-ecb1-40b9-8bd0-8f0f488456ed" />

comm file1 file2
 ## OUTPUT
 <img width="642" height="252" alt="image" src="https://github.com/user-attachments/assets/c4727c11-3610-4be8-bd31-ab6ea75875fc" />


 
diff file1 file2
## OUTPUT
<img width="597" height="235" alt="image" src="https://github.com/user-attachments/assets/3d96c312-07c4-43af-bab6-d5e158b2ddad" />



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
<img width="716" height="80" alt="image" src="https://github.com/user-attachments/assets/a759def6-16f6-479c-88d9-f873c3c60b06" />

cut -d "|" -f 1 file22
## OUTPUT
<img width="670" height="96" alt="image" src="https://github.com/user-attachments/assets/2526a247-c03e-44c2-b57b-3a3b75e422a4" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="652" height="95" alt="image" src="https://github.com/user-attachments/assets/60cc0d62-4bca-4bd2-97b3-90e68fabecaf" />


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
<img width="627" height="47" alt="image" src="https://github.com/user-attachments/assets/8d7935bc-c13a-41e0-96bc-9c8b966b4c03" />

grep hello newfile 
## OUTPUT
<img width="627" height="46" alt="image" src="https://github.com/user-attachments/assets/8e10db53-b1c2-4606-8743-219eafc63e9d" />

grep -v hello newfile 
## OUTPUT
<img width="635" height="51" alt="image" src="https://github.com/user-attachments/assets/10fa2bea-74de-48b8-b2be-6b625e6de7d9" />

cat newfile | grep -i "hello"
## OUTPUT
<img width="747" height="67" alt="image" src="https://github.com/user-attachments/assets/d9946294-912f-49cb-86a3-4822995b4c33" />

cat newfile | grep -i -c "hello"
## OUTPUT
<img width="832" height="50" alt="image" src="https://github.com/user-attachments/assets/48819256-af74-4bf6-97bf-762851218d8b" />

grep -R ubuntu /etc
## OUTPUT
<img width="942" height="862" alt="image" src="https://github.com/user-attachments/assets/77589148-5885-4007-80df-b4ba47f8ea3f" />

grep -w -n world newfile   
## OUTPUT
<img width="775" height="72" alt="image" src="https://github.com/user-attachments/assets/f8c04e55-aed9-4e68-b796-2fb9be738c21" />

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
<img width="765" height="75" alt="image" src="https://github.com/user-attachments/assets/cb61bc80-8bb7-4b99-88b3-c370f4ebcb01" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="817" height="62" alt="image" src="https://github.com/user-attachments/assets/af96a55a-6397-489c-bb05-b3476506ad8d" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="856" height="72" alt="image" src="https://github.com/user-attachments/assets/34ac9324-e56b-4592-a7be-b667e5a56f84" />

egrep '(^hello)' newfile 
## OUTPUT
<img width="705" height="52" alt="image" src="https://github.com/user-attachments/assets/2eae4dfc-abd0-4ebc-8c6a-d1b7f9a3db1b" />

egrep '(world$)' newfile 
## OUTPUT
<img width="697" height="65" alt="image" src="https://github.com/user-attachments/assets/2324df56-daac-41be-960f-7988d8fad09a" />

egrep '(World$)' newfile 
## OUTPUT
<img width="776" height="47" alt="image" src="https://github.com/user-attachments/assets/479a0217-4a04-47a4-a673-aaee717cbf12" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="757" height="75" alt="image" src="https://github.com/user-attachments/assets/8e08fa34-5cc8-489f-acdb-0a3728a26d7a" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="647" height="51" alt="image" src="https://github.com/user-attachments/assets/2653b14d-2a8e-40c0-9ae2-e71e2893e339" />

egrep 'Linux.*world' newfile 
## OUTPUT
<img width="747" height="52" alt="image" src="https://github.com/user-attachments/assets/6b142ca5-8b7f-45e7-badb-b2bba1f31e38" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="716" height="50" alt="image" src="https://github.com/user-attachments/assets/7887c755-22e3-4824-9bca-816c36da9083" />

egrep l{2} newfile
## OUTPUT
<img width="602" height="67" alt="image" src="https://github.com/user-attachments/assets/c3b068a6-f8d1-4d16-ae4c-1ebcba5bb4b7" />

egrep 's{1,2}' newfile
## OUTPUT 
<img width="726" height="97" alt="image" src="https://github.com/user-attachments/assets/845da225-0f91-48bc-87e4-d6de6d54b795" />

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
<img width="645" height="45" alt="image" src="https://github.com/user-attachments/assets/35ee41f5-2ece-4c46-a64c-2b1e2867ec66" />

sed -n -e '$p' file23
## OUTPUT
<img width="637" height="56" alt="image" src="https://github.com/user-attachments/assets/b3c22c64-b447-4334-95bf-0478fa30085c" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="756" height="212" alt="image" src="https://github.com/user-attachments/assets/d04fce3a-35d8-449c-a61f-478a439ece00" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="752" height="212" alt="image" src="https://github.com/user-attachments/assets/b97d9a49-045a-4ed7-89e5-7eb5f73539d0" />

sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="765" height="215" alt="image" src="https://github.com/user-attachments/assets/13e15662-66a7-4b63-90b2-a09050f53c0b" />

sed -n -e '1,5p' file23
## OUTPUT
<img width="721" height="135" alt="image" src="https://github.com/user-attachments/assets/d9c568de-7bc6-4229-9c79-2c031b9f7d33" />

sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="777" height="97" alt="image" src="https://github.com/user-attachments/assets/6f1db85e-e31e-4c62-80d7-224fb12f61b3" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="890" height="75" alt="image" src="https://github.com/user-attachments/assets/6d902181-0967-4c23-8331-6c62d28eb078" />

seq 10 
## OUTPUT
<img width="720" height="252" alt="image" src="https://github.com/user-attachments/assets/c2d0fff4-d63b-4292-85df-fed52b7ccbe9" />


seq 10 | sed -n '4,6p'
## OUTPUT
<img width="662" height="95" alt="image" src="https://github.com/user-attachments/assets/ac9392ec-bdf0-4cf9-858c-3ed64475433e" />

seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="671" height="92" alt="image" src="https://github.com/user-attachments/assets/f927c8b2-50ef-40ce-a787-f4b1300fbc77" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="632" height="117" alt="image" src="https://github.com/user-attachments/assets/fdd69dcd-6f0b-4264-8889-3e3e9ab0ddec" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="682" height="92" alt="image" src="https://github.com/user-attachments/assets/8aa2e7c4-cb45-4770-8776-1fac15040dcf" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="720" height="90" alt="image" src="https://github.com/user-attachments/assets/2029e401-cfde-456b-9149-328cad8f180d" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="737" height="96" alt="image" src="https://github.com/user-attachments/assets/1a8097a3-6fcf-49e8-8726-35a7f6eb1e42" />

sed -n '2,4{s/$/*/;p}' file23
<img width="805" height="96" alt="image" src="https://github.com/user-attachments/assets/164dc5b3-36f4-4746-abaa-4cc103b9f594" />

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
<img width="777" height="142" alt="image" src="https://github.com/user-attachments/assets/cc09625a-b9c9-46c9-93ac-0fdb0aa1bba6" />

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
<img width="542" height="142" alt="image" src="https://github.com/user-attachments/assets/3082de58-8580-4880-9402-0d982aabd597" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="820" height="206" alt="image" src="https://github.com/user-attachments/assets/f46ba118-6aeb-4577-b9c3-b38fa3919aae" />

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
