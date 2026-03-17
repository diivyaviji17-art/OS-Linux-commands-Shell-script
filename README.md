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
<img width="501" height="142" alt="Screenshot 2026-03-17 011319" src="https://github.com/user-attachments/assets/176661c5-1c55-4902-b90d-5fede01302a7" />



cat < file2
## OUTPUT
<img width="555" height="240" alt="Screenshot 2026-03-17 011500" src="https://github.com/user-attachments/assets/9818994d-6255-41ea-b273-2cb9ab8894e0" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="616" height="80" alt="Screenshot 2026-03-17 011633" src="https://github.com/user-attachments/assets/f1c9d204-4c01-4a66-9ecd-fbee99d3e135" />

comm file1 file2
 ## OUTPUT
<img width="646" height="337" alt="Screenshot 2026-03-17 011718" src="https://github.com/user-attachments/assets/ddae7223-9919-40f0-99e9-d922e32dc152" />

 
diff file1 file2
## OUTPUT
<img width="686" height="400" alt="Screenshot 2026-03-17 011845" src="https://github.com/user-attachments/assets/b8447299-be10-4432-846c-86a5204376b4" />


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
<img width="560" height="118" alt="Screenshot 2026-03-17 012027" src="https://github.com/user-attachments/assets/328d565a-b60d-4bd6-be46-e6d60f25df0c" />




cut -d "|" -f 1 file22
## OUTPUT


<img width="635" height="151" alt="image" src="https://github.com/user-attachments/assets/6e8dc59e-d213-459a-a32d-8c497d34680d" />

cut -d "|" -f 2 file22
## OUTPUT
<img width="633" height="144" alt="Screenshot 2026-03-17 012210" src="https://github.com/user-attachments/assets/ecaf40a3-d3cf-4495-ad12-858bb75367d8" />


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
<img width="650" height="93" alt="Screenshot 2026-03-17 012313" src="https://github.com/user-attachments/assets/5a74ba4b-9fa2-42da-98d9-c6b61d74740c" />



grep hello newfile 
## OUTPUT
<img width="633" height="83" alt="Screenshot 2026-03-17 012327" src="https://github.com/user-attachments/assets/d81a785f-59a1-4736-b846-ae609eaeda6e" />




grep -v hello newfile 
## OUTPUT
<img width="649" height="95" alt="Screenshot 2026-03-17 012339" src="https://github.com/user-attachments/assets/43abd436-7502-4e18-ad8b-962da3b5751f" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="806" height="115" alt="Screenshot 2026-03-17 012510" src="https://github.com/user-attachments/assets/f6fcdd1f-60be-4122-89d8-ea24a863a045" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="837" height="60" alt="Screenshot 2026-03-17 012615" src="https://github.com/user-attachments/assets/5c53019f-89dd-4176-afc9-69d8f57bcaf2" />




grep -R ubuntu /etc
## OUTPUT
<img width="935" height="280" alt="Screenshot 2026-03-17 012715" src="https://github.com/user-attachments/assets/18c8b146-af71-4d54-b697-3bf433d039de" />



grep -w -n world newfile   
## OUTPUT
<img width="893" height="121" alt="Screenshot 2026-03-17 012804" src="https://github.com/user-attachments/assets/90c537bf-d7d2-496b-a840-89cea5a3cae7" />


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
<img width="939" height="128" alt="Screenshot 2026-03-17 012910" src="https://github.com/user-attachments/assets/33dbfb2d-88b6-4e9f-93bd-4265b29e10fa" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="903" height="129" alt="Screenshot 2026-03-17 012949" src="https://github.com/user-attachments/assets/aceacea1-7bc7-4202-b217-1b802cf82a2a" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="908" height="124" alt="Screenshot 2026-03-17 013036" src="https://github.com/user-attachments/assets/f94588a4-d943-490b-9b51-5dae7a63a960" />




egrep '(^hello)' newfile 
## OUTPUT

<img width="860" height="101" alt="Screenshot 2026-03-17 013117" src="https://github.com/user-attachments/assets/d1ba3fca-a137-47fb-afde-2ee3ead9e9cc" />


egrep '(world$)' newfile 
## OUTPUT
<img width="881" height="73" alt="Screenshot 2026-03-17 105824" src="https://github.com/user-attachments/assets/d32ddc74-d28e-4cf5-a0f0-7d312aa50ed8" />



egrep '(World$)' newfile 
## OUTPUT

<img width="927" height="77" alt="Screenshot 2026-03-17 105913" src="https://github.com/user-attachments/assets/846c24ee-4416-4488-8de3-f3db8d019cbc" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="821" height="127" alt="Screenshot 2026-03-17 105943" src="https://github.com/user-attachments/assets/d5518be7-beae-41d0-9af5-e51bdcf5b83a" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="933" height="85" alt="Screenshot 2026-03-17 110023" src="https://github.com/user-attachments/assets/8e742aaf-c415-4b9d-9e9c-d79d9bbaefe2" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="779" height="77" alt="Screenshot 2026-03-17 110114" src="https://github.com/user-attachments/assets/94c7a3ec-d2e4-49eb-8d06-c44502c52035" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="812" height="82" alt="Screenshot 2026-03-17 110158" src="https://github.com/user-attachments/assets/714c81a1-228e-46f1-ba48-ed487cb78280" />


egrep l{2} newfile
## OUTPUT
<img width="942" height="105" alt="Screenshot 2026-03-17 110254" src="https://github.com/user-attachments/assets/c7ffd2c3-5bf1-4a54-a408-9342a36edb1f" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="921" height="143" alt="Screenshot 2026-03-17 110316" src="https://github.com/user-attachments/assets/45c2b9af-98c7-4a56-bc2b-4e3991ca35c4" />

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
<img width="644" height="75" alt="Screenshot 2026-03-17 110458" src="https://github.com/user-attachments/assets/c0723d75-8665-4474-9377-43b3211c98d4" />



sed -n -e '$p' file23
## OUTPUT
<img width="661" height="67" alt="Screenshot 2026-03-17 110513" src="https://github.com/user-attachments/assets/22c08a0d-583a-420c-a1e3-4c81a9eb45bd" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="739" height="319" alt="Screenshot 2026-03-17 110637" src="https://github.com/user-attachments/assets/6d03e1f1-2a77-4dcb-a13f-5424986ed7d7" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="715" height="344" alt="Screenshot 2026-03-17 110723" src="https://github.com/user-attachments/assets/e456e4b6-e543-41e2-973a-bfaff47c6d61" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="805" height="336" alt="Screenshot 2026-03-17 110756" src="https://github.com/user-attachments/assets/1995c7d5-bb4e-4bde-a56f-fedb06448971" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="798" height="213" alt="Screenshot 2026-03-17 110807" src="https://github.com/user-attachments/assets/e73e91a2-efae-47f1-8baa-e0193688e009" />



sed -n -e '2,/Joe/p' file23
## OUTPUT



<img width="736" height="139" alt="Screenshot 2026-03-17 110817" src="https://github.com/user-attachments/assets/3fe1d75e-4b2b-4adb-b714-b34efdc9e64c" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="780" height="95" alt="Screenshot 2026-03-17 110832" src="https://github.com/user-attachments/assets/27d4c966-99d7-4729-b039-d1a07247bf26" />



seq 10 
## OUTPUT
<img width="704" height="357" alt="Screenshot 2026-03-17 111122" src="https://github.com/user-attachments/assets/8d774b23-96e8-452a-a5ce-2275e863f8df" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="803" height="155" alt="Screenshot 2026-03-17 111204" src="https://github.com/user-attachments/assets/2c9337e3-c642-415e-b1ef-5d6ffb541a07" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="743" height="138" alt="Screenshot 2026-03-17 111218" src="https://github.com/user-attachments/assets/b79fd0f4-6ecb-45fc-89ea-c69f36b35a3e" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="800" height="145" alt="Screenshot 2026-03-17 111333" src="https://github.com/user-attachments/assets/41582c6c-8f50-465f-b364-1c620935ad16" />


seq 2 | sed '2i hello'
## OUTPUT
<img width="753" height="171" alt="Screenshot 2026-03-17 111350" src="https://github.com/user-attachments/assets/bbeb045f-f869-4862-adec-acf7f29b775d" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="731" height="148" alt="Screenshot 2026-03-17 111400" src="https://github.com/user-attachments/assets/983d8e6a-7064-49f7-a8d0-4f91e67996d0" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="808" height="142" alt="Screenshot 2026-03-17 111520" src="https://github.com/user-attachments/assets/8546b06a-cb4a-494a-87c2-d1cb7dcefba9" />



sed -n '2,4{s/$/*/;p}' file23

<img width="801" height="137" alt="Screenshot 2026-03-17 111531" src="https://github.com/user-attachments/assets/60633037-b4e6-4c8f-bd29-a1d88fb0c120" />

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
<img width="516" height="228" alt="Screenshot 2026-03-17 111654" src="https://github.com/user-attachments/assets/16951778-2986-47f0-a628-4a25e8efe215" />


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
<img width="547" height="216" alt="Screenshot 2026-03-17 111719" src="https://github.com/user-attachments/assets/7177dc6b-b9a4-48a7-a766-faa653023c33" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="904" height="324" alt="Screenshot 2026-03-17 111729" src="https://github.com/user-attachments/assets/8b86b513-fcfd-4d21-9980-abdf6132a5db" />

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

<img width="935" height="152" alt="Screenshot 2026-03-17 111746" src="https://github.com/user-attachments/assets/a236d594-014e-47f4-8c8c-a554f44b3caa" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="941" height="144" alt="Screenshot 2026-03-17 112127" src="https://github.com/user-attachments/assets/6b72575f-4bab-4026-9ca7-2b066d0d3904" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="480" height="98" alt="Screenshot 2026-03-17 112142" src="https://github.com/user-attachments/assets/d86e3299-ad57-4162-b88a-c72b9299d5f4" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="509" height="101" alt="Screenshot 2026-03-17 112152" src="https://github.com/user-attachments/assets/973be626-6c57-4058-bb35-7690e3f00fa9" />

tar -xvf backup.tar
## OUTPUT
<img width="948" height="175" alt="Screenshot 2026-03-17 112218" src="https://github.com/user-attachments/assets/20ea80ce-5f97-4c08-8a71-89eb13459beb" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="942" height="188" alt="Screenshot 2026-03-17 112454" src="https://github.com/user-attachments/assets/671263b2-532d-4cdf-af14-458b8e258f9a" />

gunzip backup.tar.gz
## OUTPUT
<img width="944" height="268" alt="Screenshot 2026-03-17 112512" src="https://github.com/user-attachments/assets/650567b7-338f-429c-9da1-d5934dfd9c25" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="954" height="393" alt="Screenshot 2026-03-17 112530" src="https://github.com/user-attachments/assets/b21a8915-1e1d-4e71-a6d3-b7dddfd4d9f3" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="555" height="143" alt="Screenshot 2026-03-17 112545" src="https://github.com/user-attachments/assets/6a75687f-7728-46f1-835c-040b04127d97" />


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
<img width="713" height="534" alt="Screenshot 2026-03-17 112601" src="https://github.com/user-attachments/assets/f06fbe39-2c59-4eec-89a4-38aa3fc9fc38" />

 
ls file1
## OUTPUT
<img width="446" height="84" alt="Screenshot 2026-03-17 112839" src="https://github.com/user-attachments/assets/487144c3-1dd2-4e4c-98f8-5fc5011e5e04" />

echo $?
## OUTPUT 
<img width="445" height="73" alt="Screenshot 2026-03-17 112851" src="https://github.com/user-attachments/assets/cb0689e3-7af8-46e5-8f45-f1d32697d663" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="412" height="76" alt="Screenshot 2026-03-17 112905" src="https://github.com/user-attachments/assets/a268a120-2b84-4336-bc82-84d5c8c8f950" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="801" height="357" alt="Screenshot 2026-03-17 113047" src="https://github.com/user-attachments/assets/d8458d49-05fa-4913-ae74-0a8879ce8a55" />


 
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
<img width="818" height="404" alt="Screenshot 2026-03-17 113253" src="https://github.com/user-attachments/assets/e7b75e82-920f-4063-90f6-f3375db2dda0" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="951" height="378" alt="Screenshot 2026-03-17 113415" src="https://github.com/user-attachments/assets/e4c17845-f624-4040-b14e-1625ff1d8608" />


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
<img width="657" height="193" alt="Screenshot 2026-03-17 113618" src="https://github.com/user-attachments/assets/20ce64fe-a702-40b3-af45-6dd833fe8d66" />

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
<img width="605" height="473" alt="Screenshot 2026-03-17 113635" src="https://github.com/user-attachments/assets/1fcab895-bdba-48b7-bea0-cedcbb5829ea" />



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
<img width="634" height="550" alt="Screenshot 2026-03-17 113649" src="https://github.com/user-attachments/assets/b01959b3-ac39-410c-8265-6cf07e4e1005" />

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
<img width="651" height="550" alt="Screenshot 2026-03-17 113704" src="https://github.com/user-attachments/assets/7bfbce2a-3d4d-4686-9ba8-6d3e926c0839" />

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
<img width="575" height="500" alt="Screenshot 2026-03-17 114055" src="https://github.com/user-attachments/assets/85e6dc0c-00a2-42ff-83b9-516595dd29fc" />


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
<img width="522" height="264" alt="Screenshot 2026-03-17 114105" src="https://github.com/user-attachments/assets/3e16dcdd-5ae1-4a82-bc41-88d27c307150" />

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
 <img width="485" height="149" alt="Screenshot 2026-03-17 114534" src="https://github.com/user-attachments/assets/907b4cc0-d30b-444e-abaf-d12143f2d370" />

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
## OUTPUT
<img width="434" height="213" alt="Screenshot 2026-03-17 114625" src="https://github.com/user-attachments/assets/5097daa5-141e-4c9f-b3ff-5cc0a6c9e68f" />

 
 
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
<img width="407" height="219" alt="Screenshot 2026-03-17 121121" src="https://github.com/user-attachments/assets/e522e905-afd7-4651-bb7c-0309d2397c85" />


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
<img width="596" height="237" alt="Screenshot 2026-03-17 120935" src="https://github.com/user-attachments/assets/071a5c99-178c-44e3-ae46-065301b81633" />

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
<img width="590" height="218" alt="Screenshot 2026-03-17 120814" src="https://github.com/user-attachments/assets/b59266e0-ac2c-41b1-a9d1-a625db893142" />

 
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
<img width="596" height="221" alt="Screenshot 2026-03-17 120707" src="https://github.com/user-attachments/assets/e2d9a8b0-4eaa-4306-a283-9a3c110fe8a5" />

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
 <img width="585" height="222" alt="Screenshot 2026-03-17 120604" src="https://github.com/user-attachments/assets/46ed6af6-3335-40b8-bb1c-4528416ffcab" />

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
<img width="465" height="139" alt="Screenshot 2026-03-17 120358" src="https://github.com/user-attachments/assets/a3f53d86-7f1f-411a-8fd3-ae407f2dcf5c" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="519" height="111" alt="Screenshot 2026-03-17 120345" src="https://github.com/user-attachments/assets/4959a83f-07a9-4d1a-8d3b-a04982c91b22" />


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
<img width="669" height="27" alt="Screenshot 2026-03-17 120110" src="https://github.com/user-attachments/assets/e9bdb51c-8310-4aab-ac60-531fa3306ae1" />

 
 ./funcex.sh 1 2
<img width="490" height="20" alt="Screenshot 2026-03-17 120006" src="https://github.com/user-attachments/assets/8ec471f9-5639-4590-a6f2-818ab0002d1c" />

 
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
 <img width="484" height="65" alt="Screenshot 2026-03-17 115910" src="https://github.com/user-attachments/assets/32dd4a52-4aaf-4e5e-8a97-12805292d92f" />

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
 <img width="581" height="58" alt="Screenshot 2026-03-17 115830" src="https://github.com/user-attachments/assets/12976dd9-1e5f-40bf-8250-ce0124070c6c" />

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
 <img width="887" height="362" alt="Screenshot 2026-03-17 105152" src="https://github.com/user-attachments/assets/1fa60ccc-4cd8-47ed-9e0b-6aa6cf8a9ff0" />
<img width="870" height="104" alt="Screenshot 2026-03-17 105247" src="https://github.com/user-attachments/assets/c6cd9a51-f316-4bad-bb0a-3c993a70f5a0" />

 
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
<img width="612" height="323" alt="Screenshot 2026-03-17 104806" src="https://github.com/user-attachments/assets/129ca8d3-420e-45df-aacf-dcba8f04bae1" />
 
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
<img width="768" height="92" alt="Screenshot 2026-03-17 104701" src="https://github.com/user-attachments/assets/2783b3d2-07d2-48e5-a2e1-26591983c774" />


# RESULT:
The Commands are executed successfully.
