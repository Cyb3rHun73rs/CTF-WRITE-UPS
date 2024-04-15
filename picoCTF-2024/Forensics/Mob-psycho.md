# Mob psycho

## Overview
* Forensics
* 200 points
  
## Description
Can you handle APKs?

Download the android apk [here](https://artifacts.picoctf.net/c_titan/142/mobpsycho.apk).

## Hints
1. Did you know you can unzip APK files?
2. Now you have the whole host of shell tools for searching these files.

## Approach
This challenge involved an APK file that needed to be unziped as the hint suggested. 
    
    $ unzip mobpsycho.apk

Upon unzipping the file, the follwoing files and folders are obtained.

![mobpsycho](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/04db8086-f2b7-41eb-a901-c53e8956e6fe)

From the second hint, searching the files is an option. From a regular linux user this is possible and it can be done through the find command as illustrated below:

      $ find <file> 
  
Since we are dealing with files, from the CTF point of you we are looking for a file containing a flag. This let's us speculate or guess that the file may be called flag.<anyhting>

      $ find flag | grep flag
  
Grepping helps to clean the terminal by just returning the desired output in case of many output.

This command returned the following output:

![mobpsycho2](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/aecf0324-26e0-420a-9144-1ea6b9aefd65)

A file named flag.txt is available within the ./res/color/ directory. Copy the path and use the cat command to view its content.

         $ cat ./res/color/flag.txt
         7069636f4354467b6178386d433052553676655f4e5838356c346178386d436c5f62313132616535377d

The above string of hexadecimal numbers is found. It takes one to get to identify different number types and encodings. This is hexadecimal and therefore an ascii text representaion of the paired characters starting from left to right can be found. 

Decode this using CyberChef or any other decoder. Alternatively you can decode it using python script.

## Flag 
picoCTF{ax8mC0RU6ve_NX85l4ax8mCl_b112ae57}

### Solved by
* GitHub [edyedu](https://github.com/ochiengedwin)
* Portfolio [Edwin Ochieng](https://sites.google.com/view/ochiengedwin)
