# endianness-v2
## Overview
* Forensics
* 300 Points

## Description
Here's a file that was recovered from a 32-bits system that organized the bytes a weird way. We're not even sure what type of file it is.

Download it [here](https://artifacts.picoctf.net/c_titan/115/challengefile) and see what you can get out of it.

## Hints
No hints

## Approach
After downloading the file, I tried verifying the file type using several available tools such as file, binwalk tools and commands but nothing interesting cam out.

Upon using exiftool which is linux command-line tool for file metadata analysis, I got a warning that the tool was Processing JPEG-like data after unknown 1-byte header as shown below:

![endianness](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/048e1e8f-c2a1-4396-93ec-c09a49b1be6b)

This gave me a clue that I maybe working with a JPEG file. I then copied the file to a file with .jpeg as an extension to have a JPEG data. However, opening this just threw errors on the terminal as the image could not be verified.

This then calls for file bytes analysis. I acquired the header data for the jpeg file using the header command and I found this: 

    FJFIC

This looked like the bytes for the header is corrupted but a clue that it could be JFIF file which is "The JPEG File Interchange Format (JFIF) is an image file format standard published as ITU-T Recommendation T. 871 and ISO/IEC 10918-5." based on wikipedia search.

Considering endianness as this is the only clue we have from the challeng's name, the file bytes may have been inverted. You can read on how endiannes work in differednt architectures.

I used the following python script to reverse the image bytes:

    with open("flag.jpeg", "rb") as file:
    BUF = 4    
    bytes_rev = b""
    bytes_read  = bytearray(file.read(BUF))
    
    while bytes_read:
        bytes_rev += bytes_read[::-1]
        bytes_read = file.read(BUF)
    with open("modified_flag.jpeg", "wb") as newfile:
        newfile.write(bytes_rev)

The script opens the newly created file with jpeg extension and reads 4 bytes of the data at a time. Then the bytes are reversed then rewrited to a jpeg file.

This created a new file with JFIF header. 

I opened the new image with the linux default image viewer and the its contents were the flag.

## Key takeaways
1. Endianness refers to the order in which bytes are stored within larger numerical values (such as integers or floating-point numbers) in memory or in binary files. There are two main types of endianness: big-endian and little-endian.
2. Manually reversing each 4-bytes of a large file is tideous hence the need of scripting. e.g. in Python
3. For unknown files, file headers are helpful to finding the clue of the file type.

## Flag
picoCTF{cert!f1Ed_iND!4n_s0rrY_3nDian_6d3ad08e}

### Solved by
* GitHub [edyedu](https://github.com/ochiengedwin)
* Portfolio [Edwin Ochieng](https://sites.google.com/view/ochiengedwin)
