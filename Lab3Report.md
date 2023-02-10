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

In example 2, we use this command to find all the files whose file name contains "Madeira" within the `./written_2` directory. This was done by adding
asterisks at the beginning and the end of input string statement. This ensure that any file name containing the string "Maderia" will be listed out.

This specific command is useful because it can help one pinpoint where exactly a file is located as well as if it even exists within a current directory

### Alternate Commnad 2:



