# linux_cookbook

For those working command-line on linux systems. Let's call them "penguins".


A penguin should know at least basic forms of sed and awk.
Recommendation: O Reilly's  "Sed & awk Pocket Reference, 2nd edition"

Below, you can find a list of command-line tasks a penguin might have to do at least one a month.
Collected from real-world experience.


Real-world examples.

## sed command examples

substitute all dots  with nothing, i.e. remove dots. 

sed 's/\.//g' tmp.txt 

substitute beginning of line with two zeroes, i.e. insert two zeroes:

sed 's/^/00/' tmp.txt 

## unique list
get a unique version of a file
sort tmp.txt | uniq


## remove all stopped containers

List them:

docker ps -a -q --filter status=exited

Delete them:

docker rm $(docker ps -a -q --filter status=exited)

## remove dangling docker images

docker rmi $(docker images --filter "dangling=true" -q --no-trunc)



