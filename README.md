
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

<img width="297" height="197" alt="image" src="https://github.com/user-attachments/assets/1e6f4547-7d57-46a9-becf-f30f8e426ce8" />


cat < file2
## OUTPUT
<img width="375" height="259" alt="image" src="https://github.com/user-attachments/assets/38f45202-d556-428c-b9b5-3c48fadd5968" />



# Comparing Files
cmp file1 file2
## OUTPUT
<img width="442" height="93" alt="image" src="https://github.com/user-attachments/assets/10ffcc44-cdc5-4d7e-9fa6-4892aa7d9fe3" />

 
comm file1 file2
 ## OUTPUT
 

 
diff file1 file2
## OUTPUT
<img width="472" height="354" alt="image" src="https://github.com/user-attachments/assets/65e4f502-9b03-4f14-8416-2c8dde75c1db" />



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
<img width="297" height="128" alt="image" src="https://github.com/user-attachments/assets/6b79be2e-96d1-405d-8091-b1b1903cc41a" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="516" height="197" alt="image" src="https://github.com/user-attachments/assets/0d4c8b3b-8115-4676-9436-8e0651adc95d" />




cut -d "|" -f 2 file22
## OUTPUT
<img width="378" height="202" alt="image" src="https://github.com/user-attachments/assets/ba65dee4-1adf-4b1d-b52d-e9a28897407e" />



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
<img width="329" height="100" alt="image" src="https://github.com/user-attachments/assets/525c85c4-6c7b-499c-89e9-970b40698804" />




grep hello newfile 
## OUTPUT
<img width="352" height="235" alt="image" src="https://github.com/user-attachments/assets/face7f47-5b50-4a6f-9163-d0acb74767fa" />





grep -v hello newfile 
## OUTPUT
<img width="367" height="107" alt="image" src="https://github.com/user-attachments/assets/8748de23-e09d-48f6-9736-54a7f67673ca" />




cat newfile | grep -i "hello"
## OUTPUT
<img width="452" height="147" alt="image" src="https://github.com/user-attachments/assets/24fefccf-60dc-4661-87f5-aca9a581bd30" />





cat newfile | grep -i -c "hello"
## OUTPUT
<img width="508" height="110" alt="image" src="https://github.com/user-attachments/assets/c3e093e4-854c-43ad-9e9c-770c0cbe3e0c" />




grep -R ubuntu /etc
## OUTPUT
<img width="831" height="523" alt="image" src="https://github.com/user-attachments/assets/486bbb08-503a-427e-82f9-ae4d6573977d" />





grep -w -n world newfile   
## OUTPUT
<img width="426" height="144" alt="image" src="https://github.com/user-attachments/assets/e0beabc9-1c40-43a7-a3d4-6b8de260456a" />



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



egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="472" height="133" alt="image" src="https://github.com/user-attachments/assets/d6398deb-db27-4bde-a728-3c26ce090abe" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="530" height="159" alt="image" src="https://github.com/user-attachments/assets/e3deb97b-1b3e-4f5c-88a8-fd5f88f24268" />



egrep '(^hello)' newfile 
## OUTPUT
<img width="446" height="100" alt="image" src="https://github.com/user-attachments/assets/729dae38-2559-4c9d-9b65-05d874640934" />




egrep '(world$)' newfile 
## OUTPUT
<img width="386" height="125" alt="image" src="https://github.com/user-attachments/assets/35c257e4-f56a-419b-93f7-dd728faee495" />




egrep '(World$)' newfile 
## OUTPUT



egrep '((W|w)orld$)' newfile 
## OUTPUT


<img width="459" height="137" alt="image" src="https://github.com/user-attachments/assets/c733befa-429d-4790-97f6-c7cdde06dd53" />

egrep '[1-9]' newfile 
## OUTPUT
<img width="360" height="103" alt="image" src="https://github.com/user-attachments/assets/15a8db3e-02c7-4273-8e43-32ac4770def1" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="443" height="96" alt="image" src="https://github.com/user-attachments/assets/a14f70b0-eda5-4c10-a3c2-f26503e70f76" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="442" height="132" alt="image" src="https://github.com/user-attachments/assets/db5a5098-0fa4-47ad-9b94-d89c3c6a4464" />



egrep l{2} newfile
## OUTPUT
<img width="330" height="128" alt="image" src="https://github.com/user-attachments/assets/5cceac0f-1c43-4933-aff1-472086cc0e7d" />






egrep 's{1,2}' newfile
## OUTPUT 
<img width="379" height="157" alt="image" src="https://github.com/user-attachments/assets/4abbd0e1-099e-4c74-8d30-e2804be70d4e" />




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
<img width="348" height="99" alt="image" src="https://github.com/user-attachments/assets/fe009138-6a24-400f-b9dc-2223cd4a9198" />




sed -n -e '$p' file23
## OUTPUT
<img width="358" height="109" alt="image" src="https://github.com/user-attachments/assets/fdf03707-4841-42df-bc41-0bd1766c4c65" />




sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="482" height="329" alt="image" src="https://github.com/user-attachments/assets/fec9aa43-7f77-466d-b726-db8f42a3a754" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="425" height="304" alt="image" src="https://github.com/user-attachments/assets/0120cb1e-5571-42d4-836f-f377b3da88d4" />




sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="461" height="323" alt="image" src="https://github.com/user-attachments/assets/9c23b165-c4cb-403d-a324-6cc2a6810a6e" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="400" height="218" alt="image" src="https://github.com/user-attachments/assets/1495141f-a105-42d9-97e7-767ec03d3fc0" />




sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="432" height="166" alt="image" src="https://github.com/user-attachments/assets/b4808f28-f25d-496c-8296-139114dae4b8" />





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="480" height="126" alt="image" src="https://github.com/user-attachments/assets/ef395945-ccaa-423c-881a-954106dac5e9" />


seq 10 
## OUTPUT
<img width="245" height="396" alt="image" src="https://github.com/user-attachments/assets/d58abfd5-9f50-4683-9895-a77ca734e035" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="350" height="158" alt="image" src="https://github.com/user-attachments/assets/0078a22a-1868-42a9-8acb-d2b8bde717b2" />




seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="389" height="169" alt="image" src="https://github.com/user-attachments/assets/19b3a93b-b2c4-43bb-b893-dbbfa2d4b0b7" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="361" height="201" alt="image" src="https://github.com/user-attachments/assets/6c353440-e700-4fe0-ba81-10ea8009c39a" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="361" height="155" alt="image" src="https://github.com/user-attachments/assets/e8599f38-12eb-43f0-8ed4-d969df0a5d6c" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="394" height="166" alt="image" src="https://github.com/user-attachments/assets/9cdf3c94-a14c-4085-8273-74795e87ac0d" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="457" height="157" alt="image" src="https://github.com/user-attachments/assets/c0e1082c-1a02-44c9-baee-c3cc0ea74290" />




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

<img width="382" height="212" alt="image" src="https://github.com/user-attachments/assets/2853850a-5039-4859-939f-005dce7f3fc4" />

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
<img width="370" height="206" alt="image" src="https://github.com/user-attachments/assets/5f74216b-4351-4770-9704-afe9df0e56be" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
 <img width="525" height="320" alt="image" src="https://github.com/user-attachments/assets/ce0eeb23-44d9-4959-9a27-12c80c8f47fe" />


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
 <img width="422" height="162" alt="image" src="https://github.com/user-attachments/assets/f09345b0-b4ff-4728-b5d1-844e7e203144" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="597" height="165" alt="image" src="https://github.com/user-attachments/assets/3143b0c4-739d-47e7-a8cd-8b304ae653b5" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="704" height="126" alt="image" src="https://github.com/user-attachments/assets/02ead116-dbb5-4d5c-9a58-c1576b6f14f8" />



tar -xvf backup.tar
## OUTPUT
<img width="700" height="137" alt="image" src="https://github.com/user-attachments/assets/473279a7-ab8a-4dae-bb68-d86fd9387867" />


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
<img width="369" height="88" alt="image" src="https://github.com/user-attachments/assets/8c9e2806-c6d3-4899-82ed-14566b384552" />


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="337" height="178" alt="image" src="https://github.com/user-attachments/assets/497dda63-485c-465a-96e3-1edaa64e3f89" />



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
<img width="807" height="188" alt="image" src="https://github.com/user-attachments/assets/ad3d69c4-9ea3-4f66-8486-1a02fe85a437" />


 
ls file1
## OUTPUT
<img width="341" height="111" alt="image" src="https://github.com/user-attachments/assets/f70c5519-f339-4097-b84d-fd1e452fc9dd" />


echo $?
## OUTPUT 
<img width="289" height="88" alt="image" src="https://github.com/user-attachments/assets/ba41af00-27ba-4c5f-9703-57231e63bf4a" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="486" height="235" alt="image" src="https://github.com/user-attachments/assets/c8e9c539-286c-4cf8-bd84-8d1196385533" />

 
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
<img width="770" height="161" alt="image" src="https://github.com/user-attachments/assets/67d5859a-e907-466a-85c0-6f6e63bcbe0e" />


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
<img width="488" height="113" alt="image" src="https://github.com/user-attachments/assets/5f8dbbea-70db-44b9-a636-46fe69b51c81" />



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
<img width="450" height="96" alt="image" src="https://github.com/user-attachments/assets/9a9803f5-bb86-4908-8fc4-35255b391197" />

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
<img width="469" height="156" alt="image" src="https://github.com/user-attachments/assets/772a4944-a81b-4061-84f1-b070e39f9d73" />


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
<img width="479" height="165" alt="image" src="https://github.com/user-attachments/assets/695ea183-c2b1-449d-9f39-15f4a6e1779e" />


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
<img width="843" height="365" alt="image" src="https://github.com/user-attachments/assets/3da46d2a-cb1e-4793-8089-8c575124f9bc" />


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
<img width="394" height="483" alt="image" src="https://github.com/user-attachments/assets/f620468f-3d99-42bd-b2dc-5591d5e74fa2" />

 
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
<img width="462" height="701" alt="image" src="https://github.com/user-attachments/assets/d9d79085-c01f-4dec-9dbb-8d377c51b69d" />



# RESULT:
The Commands are executed successfully.
