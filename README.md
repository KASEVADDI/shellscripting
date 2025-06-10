# shellscripting
# shell scripts


[root@server-1 kasevaddi]# cat shell.sh
#!/bin/bash

#below are the variable practice

name="kasevaddi"
echo "hello! $name"

variable1="hellow $USER"
echo "$variable1"
-------------------------------

echo "current user is $USER"
echo "current home is $HOME"
echo "current shell is $SHELL"
---------------------------

echo "enter username"
read username

echo "hello $username, welcome to $SHELL"
---------------------------------------
echo "enter username"
read username

echo " hello $username, welcome to $SHELL! and Today date is $(date)"
--------------------------------
a=10
b=15
sum=$((a+b))

echo "sum of $a and $b equal to $sum"
-------------------------------------------

echo "hello $2 $1, welcome to shell $SHELL"
-------------------------------
#if-else-elfi practice

echo "enter name"
read name

if [ $name == "kase" ]; then
   echo "you are the right person"
else
   echo "you are the not correct one"
fi
--------------------------------
num=15


if [ $num -gt 15 ]; then
   echo "the number is grather than 15"
fi
---------------------------
echo "enter age"
read age

if [ $age -ge 18 ]; then
   echo "your eligible for vote"
else
   echo "you are not eligible for vote"
fi
------------------------------------
echo "enter your score"
read score

if [ $score -ge 90 ]; then
   echo "you got grade A"
elif [ $score -ge 75 ]; then
     echo "your score is grade B"
elif [ $score -ge 60 ]; then
     echo " your grade is C"
else
    echo " you failed"
fi
--------------------------------------
echo "enter username"
read username

if [ $username == "kasevaddi" ]; then
   echo " welcome kasevaddi"
elif [ $username == "manju" ]; then
   echo " welcome manju"
else
   echo " wrong user"
fi
---------
functions:

!/bin/bash
greetings() {
  echo "hellow welcome to $SHELL"
}
greetings
###############
greeting_user() {
  echo "hello: $1"
  echo "you qulified your exam: $2"
}
greeting_user "manju" "mathmatics"
##################
add() {
  sum=$(( $1 + $2 ))
  echo "$sum"
}

result=$(add 5 7)
echo "Sum is: $result"
##################

add() {
    a=5
    b=10

    sum=$((a+b))
    echo "$a and $b equl to : $sum"
}
----------------
#!/bin/bash

echo hello world!

NAME="Muthyal"
echo "my name is ${NAME}"

read -p "Enter your name: " NAME
echo "my name is $NAME, nice to meet you!"
-------------------------------------------
NUM1=31
NUM2=5
if [: "$NUM1" -gt "$NU2" :]
then
echo "$NUM1 is greater than $NUM2"
else
echo "$NUM1 is less than $NUM2"
fi
-------------------------------
FILE="text.txt"
if [ -e "$FILE" ]
then
echo "$FILE is exit"
else
echo "$FILE does not exit"
fi
----------------------
#FOR LOOP RENAMING

FILES=$(ls *.txt)
NEW="MM"
for FILE in $FILES
do
echo "renaming $FILE to mm-$FILES"
mv $FILE $NEW-$FILE
done
---------------
echo " print 1 to 10 "
for (( int=1;i<=15;i++ ))
do
echo $i
done
