# linux_cookbook

## sed command examples
substitute all dots  with nothing, i.e. remove dots. 

sed 's/\.//g' tmp.txt 

substitute beginning of line with two zeroes, i.e. insert two zeroes:

sed 's/^/00/' tmp.txt 

## unique list
get a unique version of a file
sort tmp.txt | uniq


