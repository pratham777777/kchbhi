echo "Enter a Number"
read n
echo "Enter Range"
read r
i=0
while [ $i -le $r ]
do
 echo " $n x $i = `expr $n \* $i`"
 i=`expr $i + 1`
done

ch=0
while [ $ch -ne 4 ]
do
 echo "menu"
 echo "1.factorial"
 echo "2.greatest of 3 NoS"
 echo "3.reverse of a Number"
 echo "4.exit"
 echo "Enter your choice : " 
 read ch
 case $ch in
 1)echo "Enter the No : "
 read num
 i=1
 fact=1
 while [ $i -le $num ]
 do
 fact=`expr $fact \* $i`
 i=`expr $i + 1`
 done
 echo "Factorial of $num is : $fact"
 ;;
2)echo "Enter 3 NoS : "
 read n1
 read n2
 read n3
 if [ $n1 -gt $n2 -a $n1 -gt $n3 ]
 then
 echo "$n1 is the greatest No"
 else if [ $n2 -gt $n3 -a $n2 -gt $n1 ]
 then
 echo "$n2 is the greatest No"
 else
 echo "$n3 is the greatest No"
 fi
 fi;;
 3)echo "enter number"
read num
n=$num
rev=0
while [ $num -gt 0 ]
do
s=` expr $num % 10 `
rev=` expr $rev \* 10 + $s `
num=` expr $num / 10 `
done
echo "rev = $rev"
4)exit 0;;
 esac
done



ch=0
while [ $ch -ne 4 ]
do
 echo "menu"
 echo "1. reverse of a Number"
 echo "2. even and odd numbers "
 echo "3.exit"
 echo "Enter your choice : " 
 read ch
 case $ch in
 1)echo "enter number"
read num
n=$num
rev=0
while [ $num -gt 0 ]
do
s=` expr $num % 10 `
rev=` expr $rev \* 10 + $s `
num=` expr $num / 10 `
done
echo "rev = $rev"
4)exit 0;;
 esac
done
