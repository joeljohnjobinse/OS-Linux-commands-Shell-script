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
![ex1_1](https://github.com/user-attachments/assets/26b42cf0-05d3-4d00-8cee-49462faf1a06)



cat < file2
## OUTPUT
![ex1_2](https://github.com/user-attachments/assets/bfdef0bc-396b-4484-8ec4-85316ec86dae)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![ex1_3](https://github.com/user-attachments/assets/ab636efc-4bf3-46b6-8011-887b79d18af3)

comm file1 file2
 ## OUTPUT
![ex1_4](https://github.com/user-attachments/assets/3bf967b3-7c19-4991-ac3e-1f09dd0d210d)

 
diff file1 file2
## OUTPUT
![ex1_5](https://github.com/user-attachments/assets/90961acd-12c8-4a07-b286-8ee8c6f58a3c)


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
![ex1_6](https://github.com/user-attachments/assets/0865ff30-4ed5-4847-a75a-8419ef5ec751)




cut -d "|" -f 1 file22
## OUTPUT
![ex1_7](https://github.com/user-attachments/assets/cf4d9d41-bfd2-431c-a9a6-6f6369c5eb2b)



cut -d "|" -f 2 file22
## OUTPUT
![ex1_8](https://github.com/user-attachments/assets/651c0497-0303-4f10-b5ab-f3258dbc5f44)


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
![ex1_9](https://github.com/user-attachments/assets/59b66351-bd63-405c-9324-346c91cdb2cb)



grep hello newfile 
## OUTPUT
![ex1_10](https://github.com/user-attachments/assets/adfceb16-3600-4793-ab6f-1343e923aa9f)




grep -v hello newfile 
## OUTPUT
![ex1_11](https://github.com/user-attachments/assets/590ad96f-a7a8-45e6-a8d5-249a30188e64)



cat newfile | grep -i "hello"
## OUTPUT





cat newfile | grep -i -c "hello"
## OUTPUT
![ex1_12](https://github.com/user-attachments/assets/f26345ed-82a2-47dc-82b9-becaff5967e9)




grep -R ubuntu /etc
## OUTPUT
![ex1_13](https://github.com/user-attachments/assets/3c7eda57-cefb-4d61-a313-afcd41e6efe4)



grep -w -n world newfile   
## OUTPUT
![ex1_14](https://github.com/user-attachments/assets/0c1e714c-ee29-4785-ae13-9d95f8364736)


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
![ex1_15](https://github.com/user-attachments/assets/421bda68-e06d-4363-8da2-00633819e622)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![ex1_16](https://github.com/user-attachments/assets/a4e8638c-76fe-4d9b-946f-0485663e03c5)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![ex1_17](https://github.com/user-attachments/assets/eb7d03c1-4b36-48a5-a839-056be5799865)




egrep '(^hello)' newfile 
## OUTPUT
![ex1_18](https://github.com/user-attachments/assets/cd7eadf8-50c7-415b-b74d-495b60303c98)



egrep '(world$)' newfile 
## OUTPUT
![ex1_19](https://github.com/user-attachments/assets/f8cc9009-78a3-4a34-8f40-dfe478b91575)



egrep '(World$)' newfile 
## OUTPUT
![ex1_20](https://github.com/user-attachments/assets/cdceb404-eda8-40dc-a8c0-667722ad5008)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![ex1_21](https://github.com/user-attachments/assets/d4e6ea9a-6908-40da-80a7-4fb43074b5af)



egrep '[1-9]' newfile 
## OUTPUT
![ex1_22](https://github.com/user-attachments/assets/cca73eeb-2bc2-4880-aa04-27aab911e385)



egrep 'Linux.*world' newfile 
## OUTPUT
![ex1_23](https://github.com/user-attachments/assets/df287945-db99-49b7-8f33-6b18fd75fec0)


egrep 'Linux.*World' newfile 
## OUTPUT
![ex1_24](https://github.com/user-attachments/assets/02a45dfc-b434-47ab-9e25-059bf5c5e893)


egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
![ex1_25](https://github.com/user-attachments/assets/80450203-29e3-4a59-a904-d51154f2164c)


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
![ex1_26](https://github.com/user-attachments/assets/507a9d56-79f9-47ee-82bd-91977e404993)



sed -n -e '$p' file23
## OUTPUT
![ex1_27](https://github.com/user-attachments/assets/1cd404da-0276-47b0-bcfb-cbece20d0725)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![ex1_28](https://github.com/user-attachments/assets/0510445e-1926-42c0-b9ca-93076b80041a)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![ex1_29](https://github.com/user-attachments/assets/ea912ff4-69e0-4cfa-889c-06a86bdf00d6)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![ex1_30](https://github.com/user-attachments/assets/4b97a424-c09d-4d73-b7f5-93c8a8566a3b)



sed -n -e '1,5p' file23
## OUTPUT
![ex1_31](https://github.com/user-attachments/assets/2fcbc8ff-61ab-46fd-826e-7874998f47c3)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![ex1_32](https://github.com/user-attachments/assets/4399b46f-8dee-418e-b65a-8495f058bc15)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![ex1_33](https://github.com/user-attachments/assets/b7d31ad1-3be3-41f0-9491-a7d7c42ce3c5)



seq 10 
## OUTPUT
![ex1_34](https://github.com/user-attachments/assets/97ca7589-6d73-46bc-a80f-5da72db4fe45)



seq 10 | sed -n '4,6p'
## OUTPUT
![ex1_35](https://github.com/user-attachments/assets/5ad73f33-e29c-44f6-9af9-a616d2fd5a17)



seq 10 | sed -n '2,~4p'
## OUTPUT
![ex1_36](https://github.com/user-attachments/assets/a4968b5a-4b7c-4fbc-9099-0ca4734d218a)



seq 3 | sed '2a hello'
## OUTPUT
![ex1_37](https://github.com/user-attachments/assets/a62c5664-aa21-45c9-b24c-c5cfb0e3aa2e)



seq 2 | sed '2i hello'
## OUTPUT
![ex1_38](https://github.com/user-attachments/assets/e591c7b6-618f-46fd-a8c5-2ce797a36fa9)


seq 10 | sed '2,9c hello'
## OUTPUT
![ex1_39](https://github.com/user-attachments/assets/f9164720-e227-4c38-a5e0-a19e7463766c)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![ex1_40](https://github.com/user-attachments/assets/62a6fbb2-3b29-4b33-8273-14680e166f00)



sed -n '2,4{s/$/*/;p}' file23

![ex1_41](https://github.com/user-attachments/assets/61380b48-533e-4b73-844d-cf74933692c4)


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
![ex1_42](https://github.com/user-attachments/assets/42d738b7-04d0-4a5d-9faa-704015bebb5e)


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
![ex1_43](https://github.com/user-attachments/assets/d4d9768e-ed9e-4134-a7da-f58dd08bed8c)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![ex1_44](https://github.com/user-attachments/assets/41cee308-a78c-403d-ba97-b185c56adcc5)

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
![ex1_45](https://github.com/user-attachments/assets/c135b1b5-669d-4787-87e3-ffc400491db7)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![ex1_46](https://github.com/user-attachments/assets/1b965ba8-04e1-40ee-9003-d4a8a349ed46)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![ex1_47](https://github.com/user-attachments/assets/6a8dd96b-6490-48b3-8142-9c926de573b4)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![ex1_48](https://github.com/user-attachments/assets/c7fd5368-2ace-4200-8f6e-de42f42fe1b3)


tar -xvf backup.tar
## OUTPUT
![ex1_49](https://github.com/user-attachments/assets/6e29c0cd-0824-49fc-b3d3-a06668630c83)

gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
![ex1_77](https://github.com/user-attachments/assets/e8894ae2-b053-4ac1-bdba-1208891c8786)

 
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
![ex1_50](https://github.com/user-attachments/assets/86c938c1-6c8f-45b3-99d0-7746f596d9c7)


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
![ex1_51](https://github.com/user-attachments/assets/fe062df9-bba6-4a46-be44-55259ca85f6e)

 
ls file1
## OUTPUT
![ex1_52](https://github.com/user-attachments/assets/54549d08-7e77-49f0-8c52-8a13d415e311)

echo $?
## OUTPUT 
![ex1_53](https://github.com/user-attachments/assets/323888fb-36f5-439c-9322-2e2081e3298c)

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
## OUTPUT



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![ex1_54](https://github.com/user-attachments/assets/2b6a9302-21e6-4cca-9db1-56bfcfd2d737)


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
![ex1_55](https://github.com/user-attachments/assets/c506fb98-480e-4a3f-999c-df04a42eb9c6)

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
![ex1_56](https://github.com/user-attachments/assets/44af8bd5-5ca9-434a-be55-3256ec212b60)



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
![ex1_57](https://github.com/user-attachments/assets/ba7803f4-1bdb-406b-b469-cf7a6759dc49)

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
![ex1_58](https://github.com/user-attachments/assets/5d323410-dfe6-4243-8e6f-56fb3eb47575)

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
![ex1_59](https://github.com/user-attachments/assets/ce9b8dbb-4f73-4505-bc79-006d88a6e7bb)


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
![ex1_60](https://github.com/user-attachments/assets/20ad6b53-088d-4469-b98f-61df0d4740af)

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
 ![ex1_61](https://github.com/user-attachments/assets/ac145c88-9e65-408f-9761-974526fe3d39)

 
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
![ex1_62](https://github.com/user-attachments/assets/975cbadc-7b37-4ab0-9914-25bdbc014028)

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
![ex1_63](https://github.com/user-attachments/assets/bcca2377-44d0-46f5-b711-6c8480027cac)


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
![ex1_64](https://github.com/user-attachments/assets/d128e02b-0a72-4706-bdc0-e13de1ae858d)

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
![ex1_65](https://github.com/user-attachments/assets/6cb34365-0908-464a-a046-c5f4a4516b55)

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
![ex1_66](https://github.com/user-attachments/assets/2abc351a-0a6d-459c-9e70-4c98b181b5bc)

 
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
 ![ex1_67](https://github.com/user-attachments/assets/cec95e70-6175-4502-a213-76b222c7848f)

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
 ![ex1_68](https://github.com/user-attachments/assets/7eabe7b2-559a-49c7-9ffb-fe99e0a33ad0)

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
![ex1_69](https://github.com/user-attachments/assets/c2081f3c-bd02-4506-93a3-8f0606ccdb68)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

$ ./exread1.sh 

 ## OUTPUT
 ![ex1_70](https://github.com/user-attachments/assets/e955405b-5272-4337-9ac8-72f8878275be)

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
![ex1_71](https://github.com/user-attachments/assets/5ad396d4-82c6-47ee-b130-fd78e7f0dac9)

 
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
![ex1_72](https://github.com/user-attachments/assets/a8b15835-e5a6-44ee-b9be-17adc44c34c6)

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
![ex1_73](https://github.com/user-attachments/assets/1511f5b0-6513-4dcf-929e-c2ac631a89db)

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
 ![ex1_74](https://github.com/user-attachments/assets/beb7bd42-0f95-4d7d-817c-399ef0f99589)

 
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
![ex1_75](https://github.com/user-attachments/assets/f1b327af-65be-4ca8-b04d-966c31ef11c0)

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
![ex1_76](https://github.com/user-attachments/assets/42836331-49bb-4d56-ae1e-c032260d68a7)


# RESULT:
The Commands are executed successfully.
