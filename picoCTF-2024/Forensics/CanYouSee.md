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

![Screenshot (406)](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/974a994d-eab2-4498-a9d6-3969242a5a6b)
      

4. decode from base64

![one](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/0331b724-ffe4-49f5-8eb2-29e379cb7c15) 

## flag
    picoCTF{ME74D47A_HIDD3N_b32040b8}

### solved by 
* git hub &rarr; [Samuel](https://github.com/ssammueel)<br>
* portfolio &rarr; [Samuel portfolio](https://ssammueel.github.io/samuel.github.io/)
