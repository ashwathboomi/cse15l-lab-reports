# CSE 15L Lab Report 3: Researching Commands

## Learning more about the `find` command line operation:

### Alternative Command 1:

`find -name "<Input>"`

Example 1:

```
$ find -name "*.txt"
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Berk/ch2.txt
./non-fiction/OUP/Berk/CH4.txt
./non-fiction/OUP/Berk/ch7.txt
./non-fiction/OUP/Castro/chA.txt
./non-fiction/OUP/Castro/chB.txt
./non-fiction/OUP/Castro/chC.txt
./non-fiction/OUP/Castro/chL.txt
./non-fiction/OUP/Castro/chM.txt
./non-fiction/OUP/Castro/chN.txt
...
```

Example 2:

```
$ find -name "*Madeira*"
./travel_guides/berlitz1/HandRMadeira.txt
./travel_guides/berlitz1/HistoryMadeira.txt
./travel_guides/berlitz1/IntroMadeira.txt
./travel_guides/berlitz1/WhatToMadeira.txt
./travel_guides/berlitz1/WhereToMadeira.txt
```

The `find -name "<Input>"` command line operation finds and lists files within the current directory that has the same name as the input string.

In example 1, we used this command to find all the .txt files within the `./written_2` directory. This was done by adding an asterisk at the beginning of the string
statement, which means to find any file names that end with ".txt".

In example 2, we used this command to find all the files whose file name contains "Madeira" within the `./written_2` directory. This was done by adding
asterisks at the beginning and the end of input string statement. This ensure that any file name containing the string "Maderia" will be listed out.

This specific command is useful because it can help one pinpoint where exactly a file is located as well as if it even exists within a current directory

### Alternate Command 2:

`find -type <char>`

Example 1:

```
$ find -type f
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Berk/ch2.txt
./non-fiction/OUP/Berk/CH4.txt
./non-fiction/OUP/Berk/ch7.txt
./non-fiction/OUP/Castro/chA.txt
./non-fiction/OUP/Castro/chB.txt
./non-fiction/OUP/Castro/chC.txt
./non-fiction/OUP/Castro/chL.txt
./non-fiction/OUP/Castro/chM.txt
./non-fiction/OUP/Castro/chN.txt
./non-fiction/OUP/Castro/chO.txt
./non-fiction/OUP/Castro/chP.txt
...
```

Example 2:

```
$ find -type d
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Berk
./non-fiction/OUP/Castro
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Rybczynski
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz2
```

The `find -type <char>` command line operation finds all the files within a directory of a specific type (file, directory, block special, etc.)

In example 1, we used this command to find all the files within the `./written_2` directory. In this case, there were only .txt files within the directory. 
If there were other file types within the directory then they would also be listed. We did this by using the character `f` after the type command.

In example 2, we used this command to find all the directories within the `./written_2` directory. As you can see, it even lists the current written_2 directory.
We did this by using the character `d` after the type command.

Other operators that can be used are b(block special, c(character special), p(named pipe).

This command is useful because it helps one see what are all the possible locations within a directory and can help troubleshoot if there is a directory in the 
wrong location.

### Alternate Command 3:

`find -size <char>`

Example 1:

```
find -size +1000c
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Berk/ch2.txt
./non-fiction/OUP/Berk/CH4.txt
./non-fiction/OUP/Berk/ch7.txt
./non-fiction/OUP/Castro/chA.txt
./non-fiction/OUP/Castro/chB.txt
./non-fiction/OUP/Castro/chC.txt
...
```

Example 2:

```
$ find -size -1000c
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Berk
./non-fiction/OUP/Castro
./non-fiction/OUP/Fletcher
./non-fiction/OUP/Kauffman
./non-fiction/OUP/Rybczynski
./travel_guides
./travel_guides/berlitz1
./travel_guides/berlitz1/HandRIbiza.txt
./travel_guides/berlitz1/HandRIstanbul.txt
./travel_guides/berlitz2
```

The `find -size <char>` command line operation lists files/directories that meet the specified size argument set by the user.

In example 1, we used this command to find all files/directories within `./written_2` directory that are over 1000 bytes in size. We did this by using the
`+1000c` command after `size`

In example 2, we used this command to find all files/directories within `./written_2` directory that are less than 1000 bytes in size. We did this by using the
`-1000c` command after `size`

Other operators that can be used are b(512 byte-size block), k(kilobytes), M(megabytes). 

This command is helpful as it can help narrow down larger files that are unused and can be deleted. 

### Alternative Command 4:

`find -used <int>`

Example 1:

```
$ find -used -10
.
./non-fiction
./non-fiction/OUP
./non-fiction/OUP/Abernathy
./non-fiction/OUP/Abernathy/ch1.txt
./non-fiction/OUP/Abernathy/ch14.txt
./non-fiction/OUP/Abernathy/ch15.txt
./non-fiction/OUP/Abernathy/ch2.txt
./non-fiction/OUP/Abernathy/ch3.txt
./non-fiction/OUP/Abernathy/ch6.txt
./non-fiction/OUP/Abernathy/ch7.txt
./non-fiction/OUP/Abernathy/ch8.txt
./non-fiction/OUP/Abernathy/ch9.txt
./non-fiction/OUP/Berk
./non-fiction/OUP/Berk/ch1.txt
./non-fiction/OUP/Berk/ch2.txt
...
```

Example 2:

```
$ find -used +10
```

The command `find -used <int>` find all the files and directories within the current directory that have been accessed in the `<int>` days.

In example 1, we used the command to find all the files and directories that have been accessed within the last 10 days. This was done by using the `-` operator 
in front of the integer number of days.

In example 2, we used the command to find all the files and directories that have been accessed more than 10 days ago. This was done by using the `+` operator in
front of the integer number of days

The `-` operator is used for finding within the last n amount of days. The `+` operator is used for finding more than n amount of days ago.

This command is useful for logging which files were accessed and when they were accessed. Its also useful for security purposes.

### References:

[man7.org](https://man7.org/linux/man-pages/man1/find.1.html)








