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

<img width="270" height="167" alt="image" src="https://github.com/user-attachments/assets/d62c53b6-b093-4fe0-a28c-06efd1d1f965" />


cat < file2
## OUTPUT

<img width="257" height="172" alt="image" src="https://github.com/user-attachments/assets/6ed32ff6-b40d-4171-95ee-91224436deca" />

# Comparing Files
cmp file1 file2
## OUTPUT

<img width="373" height="82" alt="image" src="https://github.com/user-attachments/assets/bec79c38-8797-48f2-9a5d-3e1d689dab68" />

 
comm file1 file2
 ## OUTPUT

<img width="327" height="282" alt="image" src="https://github.com/user-attachments/assets/92c85489-7aac-4d33-a94a-66f4bb9c37f1" />

 
diff file1 file2
## OUTPUT

<img width="317" height="317" alt="image" src="https://github.com/user-attachments/assets/f6cdd83c-e51e-44cc-9aa6-873c8e625a28" />


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

<img width="323" height="143" alt="image" src="https://github.com/user-attachments/assets/e14ae3b5-ab91-4c1a-a4f8-d511384c1e50" />


cut -d "|" -f 1 file22
## OUTPUT

<img width="392" height="155" alt="image" src="https://github.com/user-attachments/assets/066ba571-db29-4b52-85bc-2ae958a909e4" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="400" height="140" alt="image" src="https://github.com/user-attachments/assets/fea75e4a-e7d3-41fe-b5c9-e2d990e6e432" />


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

<img width="345" height="92" alt="image" src="https://github.com/user-attachments/assets/34b1032b-fbd9-45cf-a2b5-f2172d7624e3" />


grep hello newfile 
## OUTPUT


<img width="352" height="68" alt="image" src="https://github.com/user-attachments/assets/5f99a713-de2e-4ab9-9d18-4ac1a820d22f" />


grep -v hello newfile 
## OUTPUT

<img width="377" height="97" alt="image" src="https://github.com/user-attachments/assets/897c42b8-ffb5-4bfb-b7ec-18f8eb43e655" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="456" height="96" alt="image" src="https://github.com/user-attachments/assets/79327342-85b6-48c9-a0e5-949cf91841cf" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="498" height="77" alt="image" src="https://github.com/user-attachments/assets/81fa128e-9332-459b-a5ed-0ff536b3507c" />


grep -w -n world newfile   
## OUTPUT

<img width="402" height="105" alt="image" src="https://github.com/user-attachments/assets/cb02e011-0ff0-4dfd-899e-49fb70c0ee3f" />


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

<img width="461" height="98" alt="image" src="https://github.com/user-attachments/assets/b1a3dbf3-9cac-4d2a-be32-e815ddea3ad5" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="450" height="90" alt="image" src="https://github.com/user-attachments/assets/b04ca439-3334-46f0-8ad7-e5d4ca18ac29" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="498" height="95" alt="image" src="https://github.com/user-attachments/assets/19d38311-56f5-40c6-bfb1-0cc7b81b0362" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="425" height="76" alt="image" src="https://github.com/user-attachments/assets/b109676b-380c-4a48-972e-1bbe62067351" />


egrep '(world$)' newfile 
## OUTPUT

<img width="397" height="90" alt="image" src="https://github.com/user-attachments/assets/2835e213-3efd-494b-8c1b-a4726586fe29" />


egrep '(World$)' newfile 
## OUTPUT

<img width="408" height="68" alt="image" src="https://github.com/user-attachments/assets/2740a0d7-9b1b-4c12-9f4b-c22b79671e8f" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="442" height="117" alt="image" src="https://github.com/user-attachments/assets/09abd938-c551-49c6-8af5-57714d92f085" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="368" height="67" alt="image" src="https://github.com/user-attachments/assets/a9e16c54-f075-4592-97ea-6d1001e3f8e3" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="450" height="77" alt="image" src="https://github.com/user-attachments/assets/d72bcc6b-31a9-45bb-bfd9-d378a1ce9898" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="437" height="75" alt="image" src="https://github.com/user-attachments/assets/a3f2d71d-5b7a-4723-a746-66461fc01a50" />


egrep l{2} newfile
## OUTPUT

<img width="353" height="92" alt="image" src="https://github.com/user-attachments/assets/c620e977-9b5e-42af-8082-297ab855e649" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="396" height="120" alt="image" src="https://github.com/user-attachments/assets/0b1c3659-371f-4015-a843-1ce352260420" />

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

<img width="367" height="72" alt="image" src="https://github.com/user-attachments/assets/b688a192-a541-444d-81a1-171f6156b735" />


sed -n -e '$p' file23
## OUTPUT

<img width="382" height="82" alt="image" src="https://github.com/user-attachments/assets/79ad44bd-a780-4882-9276-737281e420ec" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="465" height="251" alt="image" src="https://github.com/user-attachments/assets/282c2f85-b6f5-417a-9f86-d59e2179a98d" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="461" height="243" alt="image" src="https://github.com/user-attachments/assets/caac46ee-fb7c-473c-87d9-eee294c04ce0" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="477" height="250" alt="image" src="https://github.com/user-attachments/assets/7899fd17-748e-4647-b4cf-2eb3835627e3" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="410" height="163" alt="image" src="https://github.com/user-attachments/assets/f0a035d4-79ed-4683-91d8-f880d14c69f4" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="428" height="120" alt="image" src="https://github.com/user-attachments/assets/c3e816e2-8775-409c-a542-db17ba76e0c1" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="486" height="95" alt="image" src="https://github.com/user-attachments/assets/8b009c89-4cb0-4903-b6e0-c78734ed81c1" />

seq 10 
## OUTPUT

<img width="297" height="265" alt="image" src="https://github.com/user-attachments/assets/cf36eb50-f6dd-4f4d-8e69-fc204afedee4" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="376" height="113" alt="image" src="https://github.com/user-attachments/assets/df0fb57f-caea-417b-a363-561dfbab95a1" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="402" height="115" alt="image" src="https://github.com/user-attachments/assets/f07ec060-f57c-4347-b264-707653f61fce" />

seq 3 | sed '2a hello'
## OUTPUT

<img width="400" height="148" alt="image" src="https://github.com/user-attachments/assets/a329b14a-a802-426c-9f16-0887e49980a3" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="410" height="117" alt="image" src="https://github.com/user-attachments/assets/557a6ded-ce19-4cc1-87c2-d87cbde24b92" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="407" height="125" alt="image" src="https://github.com/user-attachments/assets/57b1d58f-f5dd-45c8-ac69-c3d19d0a8b44" />

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="462" height="117" alt="image" src="https://github.com/user-attachments/assets/7d754ce1-782d-4ae8-9d62-0bb130872cdd" />


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

<img width="327" height="177" alt="image" src="https://github.com/user-attachments/assets/3986c292-e557-428b-8567-19afb467fb1e" />

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

<img width="423" height="150" alt="image" src="https://github.com/user-attachments/assets/5bd8b7f3-ce54-4095-92af-d06df6338bde" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="532" height="242" alt="image" src="https://github.com/user-attachments/assets/7c7b9fe8-0362-4e81-ba0a-cc5daf3d0d83" />


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

<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/8487323b-34e0-42c6-87b2-aafb45524431" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="555" height="147" alt="image" src="https://github.com/user-attachments/assets/9ba4b026-20a2-417f-b60d-2239d2e6d598" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="371" height="251" alt="image" src="https://github.com/user-attachments/assets/cb8f4b30-3a5d-4c4d-8325-54c59e73538c" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="645" height="305" alt="image" src="https://github.com/user-attachments/assets/6391a011-6ece-40cb-9063-ed43151eae0c" />


tar -xvf backup.tar
## OUTPUT

<img width="438" height="245" alt="image" src="https://github.com/user-attachments/assets/446ac3e5-84fb-4590-840d-1c29a9364ebf" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="337" height="136" alt="image" src="https://github.com/user-attachments/assets/5d8e8ad7-1b82-4f07-9751-db420669905b" />

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

 <img width="503" height="865" alt="image" src="https://github.com/user-attachments/assets/ad47d37b-1006-45d0-a584-c6d0cb2d55ae" />

ls file1
## OUTPUT

<img width="247" height="85" alt="image" src="https://github.com/user-attachments/assets/d203cf0d-2465-4614-846a-dc2ecce0f605" />


echo $?
## OUTPUT 
./one
bash: ./one: Permission denied

<img width="220" height="67" alt="image" src="https://github.com/user-attachments/assets/ab27e735-a95e-41ff-bc18-56c387949de3" />

 echo $?
## OUTPUT 

 <img width="252" height="73" alt="image" src="https://github.com/user-attachments/assets/fbca1ac1-d016-43d5-b7c2-8af79fe3f49f" />

abcd
 
echo $?
 ## OUTPUT

<img width="302" height="87" alt="image" src="https://github.com/user-attachments/assets/0312301c-6c41-4a59-b84f-ecd5a682dea0" />

 
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

<img width="411" height="200" alt="image" src="https://github.com/user-attachments/assets/1a65d6f3-6faf-4ff8-8400-42dbbb6e3297" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="362" height="111" alt="image" src="https://github.com/user-attachments/assets/12a060d8-6bce-4ff4-a792-dbfb6e20cd13" />

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

<img width="388" height="80" alt="image" src="https://github.com/user-attachments/assets/2a1edd0a-c3ba-460d-8813-589dbfe3c526" />

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

<img width="428" height="90" alt="image" src="https://github.com/user-attachments/assets/6e8df75d-b37c-4581-8086-8077d4b30a11" />


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

<img width="393" height="127" alt="image" src="https://github.com/user-attachments/assets/2ad3fe8a-114e-4eb5-b126-ce34fa07848e" />

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

<img width="422" height="133" alt="image" src="https://github.com/user-attachments/assets/26a8b8f7-1f15-4aa8-9de6-87537dffe0b3" />

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

<img width="430" height="182" alt="image" src="https://github.com/user-attachments/assets/765436df-d6ff-4415-abf1-991ef3c17ef0" />

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

<img width="438" height="110" alt="image" src="https://github.com/user-attachments/assets/5ad0c4f1-689c-49e1-8ec1-0184f2629699" />

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

<img width="631" height="256" alt="image" src="https://github.com/user-attachments/assets/7e340f69-b00d-49f5-894d-acf7328212ea" />

cat > whiletest
```
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

<img width="377" height="305" alt="image" src="https://github.com/user-attachments/assets/92298f15-a866-4e3a-8285-31b41e27d7a5" />

cat untiltest.sh
```
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
```

$ chmod 755 untiltest.sh
## OUTPUT

<img width="435" height="160" alt="image" src="https://github.com/user-attachments/assets/12993850-2e82-4205-bfe0-ab7c16a097ad" />

cat forin1.sh
```
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

<img width="390" height="210" alt="image" src="https://github.com/user-attachments/assets/21232cb2-7aba-4151-83ec-6f414f2a3a56" />

cat forin2.sh
```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```

$ chmod 755 forin2.sh
## OUTPUT

<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/43ec8728-0339-432e-bf8d-7b43008ea0da" />
cat forin2.sh
```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh

$ ./forin2.sh

## OUTPUT

<img width="377" height="151" alt="image" src="https://github.com/user-attachments/assets/48d4f9f1-1a56-435c-9d9e-624475ed243c" />

cat forin3.sh
```
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh

## OUTPUT

<img width="405" height="218" alt="image" src="https://github.com/user-attachments/assets/ebd27018-ab56-4f83-a925-5f7af2d3601d" />

cat forin1.sh
```
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT

<img width="385" height="210" alt="image" src="https://github.com/user-attachments/assets/25447e8b-d4d1-429b-9ece-1a3bc65076f8" />

cat forinfile.sh
```
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```

$ chmod 777 forinfile.sh $ cat cities Hyderabad Alampur Basara Warangal Adilabad Bhadrachalam Khammam

## OUTPUT

<img width="298" height="71" alt="image" src="https://github.com/user-attachments/assets/aa61380c-0d75-4971-b0df-b7d1c3e3314d" />

cat forctype.sh
```
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
$ chmod 755 forctype.sh $ ./forctype.sh
## OUTPUT

<img width="393" height="200" alt="image" src="https://github.com/user-attachments/assets/466e902a-5fff-4b39-8d1b-c9d27bab7208" />

cat forctype1.sh
```
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh $ ./forctype1.sh

## OUTPUT

<img width="392" height="191" alt="image" src="https://github.com/user-attachments/assets/d4bf2ed7-1e74-4aaf-8415-f6792a231680" />

cat fornested1.sh
```
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

<img width="437" height="335" alt="image" src="https://github.com/user-attachments/assets/49a19236-70bd-4350-9ef0-9c8df44b181e" />

cat forbreak.sh
```
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
<img width="393" height="142" alt="680399722-9e44259e-4fa2-4f7c-b73c-f5283d801cdb" src="https://github.com/user-attachments/assets/0d110257-c796-42c6-b173-611f0541040c" />

$ chmod 755 forcontinue.sh

$ ./forcontinue.sh

## OUTPUT

<img width="412" height="182" alt="680400554-2d93e86c-dc4e-45dd-814e-d935b43bb1b5" src="https://github.com/user-attachments/assets/52cd1b44-36cd-41b1-bc10-b516f9c57ec3" />

cat exread.sh
```
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
```
$ chmod 755 exread.sh

$ ./exread.sh

## OUTPUT

<img width="2170" height="725" alt="image" src="https://github.com/user-attachments/assets/0475cea1-fc52-43ec-9f74-b0df791a5235" />

cat exread1.sh
```
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
```
$ chmod 755 exread1.sh

## OUTPUT

<img width="2170" height="725" alt="image" src="https://github.com/user-attachments/assets/0c0c5d48-f80b-408c-8689-e8ee4e1a612f" />

$ ./exread1.sh

cat funcex.sh
```
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

<img width="376" height="97" alt="image" src="https://github.com/user-attachments/assets/6556ad7a-86ee-4190-a68e-6dc74e497712" />

./funcex.sh 
./funcex.sh 1 2

cat argshift.sh
```
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT

<img width="396" height="143" alt="image" src="https://github.com/user-attachments/assets/4fe87b80-a950-4f3f-86f4-42e333fd85ae" />

$ ./argshift.sh 1 2 3

cat argshift1.sh
```
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

<img width="405" height="142" alt="image" src="https://github.com/user-attachments/assets/83c92dcd-edfa-4afa-aa98-9085b950cd0e" />

$ ./argshift.sh 1 2 3
cat argshift.sh
```
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT

<img width="407" height="350" alt="image" src="https://github.com/user-attachments/assets/30841155-81f2-44f9-9bf2-e868c18664d3" />

./argshift.sh 1 2 3

cat > nc.awk
```
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
```
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


<img width="376" height="65" alt="image" src="https://github.com/user-attachments/assets/a0b906d1-bc97-4784-955f-045e76776bdb" />

cat > palindrome.sh
```
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


<img width="407" height="138" alt="image" src="https://github.com/user-attachments/assets/1e66da0c-e279-4878-9fa3-793d15bce116" />

## RESULT:

The Commands are executed successfully.
