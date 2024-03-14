# infomation

## overview
* forensics
* 100 points 

## Description
CanYouSee

## Hints
How about some hide and seek?

## Approach
download the file and unzip it

     $ unzip unknown.zip 
get metadata about the image

    $ exiftool ukn_reality.jpg

    attribute url : cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==

decode from base64

    $ echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fYjMyMDQwYjh9Cg==" | base64 -d

## flag
    picoCTF{ME74D47A_HIDD3N_b32040b8}
