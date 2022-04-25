# Bash

## Get exit code
```
echo $?
```

## Date, with formatted YearMonthDay
```
date +"%Y%m%d"
date +%Y%m%d%H%M%S
```

Saving to a variable
```
export DATE=`date +"%Y%m%d"`
export DATE=`date +"+%Y%m%d%H%M%S"`
```

## Functions
How to create a bash function
* [Functions - Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/bash-functions.php)

## Multiline comments
Bash doesn't support multiline comments, but here's a hack that works.
```
<<'###BLOCK-COMMENT'
line 1
line 2
###BLOCK-COMMENT
```

## Dictionary variables
Bash does have primitive dictionary (key/value) variables in v4.0 or higher.
* [dictionaries in bash | bitarray - A guide for SRE, DevOps and Webmasters](https://www.bitarray.io/dictionaries-in-bash/)

## Finding new files
```
find . -type f -newermt "2021-11-01"
```

# Bash script snippets

Is file a directory
```
if [ -d /my/directory/ ];
then
    echo "/my/directory/ is directory"
else
    echo "/my/directory/ is not a directory"
fi
```

Pause for user input
```
# Get user input to continue or quit
read -p "Press any key to continue, q to quit> " -n 1 key
if [[ $key == 'q' ]]
then
	echo ""
	exit
elif [[ $key != '' ]]
then
	# echo blank line on any key except enter
	echo ""
fi
```
