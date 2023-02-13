# **Lab 1**

The command that I will be focusing on today is the **find** command. 

## Option 1: -empty

### Example 1
      [cs15lwi23aul@ieng6-201]:written_2:264$ find -empty
      ./lab5/emptyfile.txt
  
### Example 2
    [cs15lwi23aul@ieng6-202]:written_2:279$ find -empty
    ./non-fiction/emptyfile2.txt
    ./travel_guides/berlitz1/emptyPDF.pdf
    ./travel_guides/emptyDirectory
    ./lab5/emptyfile.txt
    
 In these examples, I have added an empty .txt file in a two seperate directories, an empty directory and an empty pdf file within a second layer of directories. The option -empty is recursively searching through all files and folders within ./written2 and is returning anything that is empty disregarding file type and a distinction between file and directory. This is useful to locate any empty files that are in your system in order to save space and clean your work space up.
 
## Option 2: -type

### Example 1
    [cs15lwi23aul@ieng6-202]:written_2:285$ find -mindepth 4 -type f
    ./non-fiction/OUP/Abernathy/ch1.txt
    ./non-fiction/OUP/Abernathy/ch14.txt
    ./non-fiction/OUP/Abernathy/ch15.txt
    ./non-fiction/OUP/Abernathy/ch2.txt
    ./non-fiction/OUP/Abernathy/ch3.txt
    ./non-fiction/OUP/Abernathy/ch6.txt
    ./non-fiction/OUP/Abernathy/ch7.txt
    ./non-fiction/OUP/Abernathy/ch8.txt
    ./non-fiction/OUP/Abernathy/ch9.txt
    ./non-fiction/OUP/Berk/CH4.txt
    ./non-fiction/OUP/Berk/ch1.txt
    ./non-fiction/OUP/Berk/ch2.txt
    ./non-fiction/OUP/Berk/ch7.txt
    ./non-fiction/OUP/Castro/chA.txt
    ./non-fiction/OUP/Castro/chB.txt
    ./non-fiction/OUP/Castro/chC.txt
    ./non-fiction/OUP/Castro/chL.txt
    ./non-fiction/OUP/Castro/chM.txt
    ./non-fiction/OUP/Castro/chN.txt
    ./non-fiction/OUP/Castro/chO.txt
    ./non-fiction/OUP/Castro/chP.txt
    ./non-fiction/OUP/Castro/chQ.txt
    ./non-fiction/OUP/Castro/chR.txt
    ./non-fiction/OUP/Castro/chV.txt
    ./non-fiction/OUP/Castro/chW.txt
    ./non-fiction/OUP/Castro/chY.txt
    ./non-fiction/OUP/Castro/chZ.txt
    ./non-fiction/OUP/Fletcher/ch1.txt
    ./non-fiction/OUP/Fletcher/ch10.txt
    ./non-fiction/OUP/Fletcher/ch2.txt
    ./non-fiction/OUP/Fletcher/ch5.txt
    ./non-fiction/OUP/Fletcher/ch6.txt
    ./non-fiction/OUP/Fletcher/ch9.txt
    ./non-fiction/OUP/Kauffman/ch1.txt
    ./non-fiction/OUP/Kauffman/ch10.txt
    ./non-fiction/OUP/Kauffman/ch3.txt
    ./non-fiction/OUP/Kauffman/ch4.txt
    ./non-fiction/OUP/Kauffman/ch5.txt
    ./non-fiction/OUP/Kauffman/ch6.txt
    ./non-fiction/OUP/Kauffman/ch7.txt
    ./non-fiction/OUP/Kauffman/ch8.txt
    ./non-fiction/OUP/Kauffman/ch9.txt
    ./non-fiction/OUP/Rybczynski/ch1.txt
    ./non-fiction/OUP/Rybczynski/ch2.txt
    ./non-fiction/OUP/Rybczynski/ch3.txt
    
### Example 2
    [cs15lwi23aul@ieng6-202]:written_2:286$ find -type d
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
    ./travel_guides/emptyDirectory
    ./lab5

The -type option allows the user to find a specific type of file with the given or current directory. It has many file type options, but the two that are used in the examples are "f" for file and "d" for directory. Using the -type options really helps with specifiying which files you are searching for if you don't know the name or location of the file. 

## Option 3: -min/maxdepth

### Example 1
      [cs15lwi23aul@ieng6-202]:written_2:288$ find -maxdepth 2 -empty
      ./non-fiction/emptyfile2.txt
      ./travel_guides/emptyDirectory
      ./lab5/emptyfile.txt
      
### Example 2
      [cs15lwi23aul@ieng6-202]:written_2:289$ find -mindepth 2 -type d
      ./non-fiction/OUP
      ./non-fiction/OUP/Abernathy
      ./non-fiction/OUP/Berk
      ./non-fiction/OUP/Castro
      ./non-fiction/OUP/Fletcher
      ./non-fiction/OUP/Kauffman
      ./non-fiction/OUP/Rybczynski
      ./travel_guides/berlitz1
      ./travel_guides/berlitz2
      ./travel_guides/emptyDirectory

The -mindepth and -maxdepth options have similar functions in that it restricts the recursive search capabilites to a certain bound by either setting a minimum or a maximum. In the examples, I have used commands that I have used in other examples with the added restirctions. The output is a list of files that fit the given criteria. This is useful if you are trying to find if files exist only a few branches down or if you want to ignore any shallow files. 

## Option 4: -mmin

### Example 1
      [cs15lwi23aul@ieng6-202]:written_2:361$ find -mmin -10
      ./non-fiction/OUP/Castro/chM.txt
      ./non-fiction/OUP/Kauffman
      ./non-fiction/OUP/Kauffman/ch1.txt
      ./non-fiction/OUP/Kauffman/chQ.txt
      ./non-fiction/emptyfile2.txt
      ./travel_guides/berlitz2/Bahamas-WhatToDo.txt
      ./travel_guides/berlitz2/Poland-History.txt
      ./lab5
      ./lab5/emptyfile.txt
      
### Example 2
      [cs15lwi23aul@ieng6-202]:written_2:363$ find -maxdepth 2 -mmin +120
      .
      ./non-fiction
      ./non-fiction/OUP
      ./travel_guides
      ./travel_guides/berlitz2
      ./travel_guides/emptyDirectory
      ./-k
      
The -mmin option finds all files/directories that have been modified within the given time frame. Inputting a number after -mmin restricts the search to files that have been modified that number of minutes ago. Adding the +/- modifier give the command a range of times to look through, + being the given time and longer and - being the given time and less. In these examples, I have modifed specific files in the last 10 minutes and they are outputted in the first command while the rest I left untouched. This is useful if you are working on a shared directory and you want to know which files have been modified recently or which ones have not been modified recently.
