# Secret Of The Polyglot

## Overview
* Forensics
* 100 Points

## Description

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?
Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/9/flag2of2-final.pdf).

## Hints
1. This problem can be solved by just opening the file in different ways

## Approach
Downloaded file is a pdf file just from the looks. Its extension is a pdf.

I gave it a try and opened it with the default pdf viewer and part of the flag was visible.

![polyglot](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/121100c0-70cf-454c-8edb-712fafb7594d)

From the hint given, this file maybe another file and to find out if this is true, I queried more info about the pdf file using file command

           $ file flag2of2-final.pdf 

This returned that the file is a png file as shown below

![polyglot2](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/2034f614-fed8-461e-9846-316320d33e71)

I copied the file and added a .png file extension and opening the photo produced the first part of the flag.

            $ cp flag2of2-final.pdf flag2of2-final.png
            $ open flag2of2-final.png

Combining the two flag parts gave a complete flag. This was a simple challenge to say.

## Flag
picoCTF{f1u3n7_1n_pn9_&_pdf_724b1287}

### Solved by 
* GitHub [edyedu](https://github.com/ochiengedwin)
* Portfolio [Edwin Ochieng](https://sites.google.com/view/ochiengedwin)
