# Scan Surprise

## overview
* forensics
* 50 points 

## Description
I've gotten bored of handing out flags as text. 
Wouldn't it be cool if they were an image instead?

challenge file [challenge.zip](https://artifacts.picoctf.net/c_atlas/14/challenge.zip)

## Hints
1. QR codes are a way of encoding data. While they're most known for storing URLs, they can store other things too.
2. Mobile phones have included native QR code scanners in their cameras since version 8 (Oreo) and iOS 11
3. If you don't have access to a phone, you can also use zbar-tools to convert an image to text

## Approach
&rarr; The challenge proved straightforward, merely requiring the user to scan a QR code in order to obtain the flag 
download the file and unzip it

     $ unzip challenge.zip 
you are given a QR code

![Screenshot (405)](https://github.com/Cyb3rHun73rs/CTF-WRITE-UPS/assets/159914996/68b467eb-2cfa-4cf5-a62f-3f261f5f2b75)

There are many ways of scanning QR codes
 *Smartphone Cameras
* QR Code Scanner Apps eg QR Code Reader & Barcode Scanner
* QR Code Scanners in Web Browsers eg Google Chrome, safari


## flag
    picoCTF{p33k_@_b00_0194a007}

### solved by 
* git hub &rarr; [Samuel](https://github.com/ssammueel)<br>
* potfolio &rarr; [Samuel potfolio](https://ssammueel.github.io/samuel.github.io/)

