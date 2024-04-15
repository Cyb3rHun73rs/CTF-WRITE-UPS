# infomation

## overview
* forensics
* 100 points 

## Description
CanYouSee

challenge file [Here](https://artifacts.picoctf.net/c_titan/128/unknown.zip)

## Hints
How about some hide and seek?

## Approach
1. download the file and unzip it

     $ unzip unknown.zip 
2. get metadata about the image

       $ exiftool ukn_reality.jpg

 3. there is someting intresting in attribute; it's a base64 encoded data

      

4. decode from base64

    $ echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==" | base64 -d

## flag
    picoCTF{ME74D47A_HIDD3N_b32040b8}
