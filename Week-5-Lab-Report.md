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
