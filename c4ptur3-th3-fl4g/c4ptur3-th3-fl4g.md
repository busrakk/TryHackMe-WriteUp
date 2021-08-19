# c4ptur3-th3-fl4g

### [Task 1] Translation & Shifting 


#####  1. Leet Conventer

```
c4n y0u c4p7u23 7h3 f149?
```

* The first question is a ciphertext related to leet encryption. 
* We can guess the answer easily or So, we can use some `online converter` like the one [here](http://www.robertecker.com/hp/research/leet-converter.php).

**Solution :** can you  capture the flag?


#####  2. Binary

```
01101100 01100101 01110100 01110011 00100000 01110100 01110010 01111001 00100000 01110011 01101111 01101101 01100101 00100000 01100010 01101001 01101110 01100001 01110010 01111001 00100000 01101111 01110101 01110100 00100001
```
* We can do the solution by decoding the given binary code with `online converters` like the one [here](https://www.rapidtables.com/convert/number/binary-to-ascii.html).

**Solution :** lets try some binary out!


#####  3. Base32
```
MJQXGZJTGIQGS4ZAON2XAZLSEBRW63LNN5XCA2LOEBBVIRRHOM======
```

* In the third question, there is a text encrypted with base32. 
* It consists of 32-char set. 
* These char-sets are usually alphabet in uppercase.
* We can use some `online decode` like the one [here](https://emn178.github.io/online-tools/base32_decode.html).
* We can easily decode this text via terminal. The command I use in terminal: 

``` 
root@busra:~$ echo "MJQXGZJTGIQGS4ZAON2XAZLSEBRW63LNN5XCA2LOEBBVIRRHOM======" | base32 -d
```

![image](https://user-images.githubusercontent.com/62840507/129717449-6beac9f9-63f5-44a6-9c57-7d9536292b98.png)

**Solution :** base32 is super common in CTF's


#####  4. Base64
```
RWFjaCBCYXNlNjQgZGlnaXQgcmVwcmVzZW50cyBleGFjdGx5IDYgYml0cyBvZiBkYXRhLg==
```
* This question, there is a text encrypted with base64 . 
* It consists of 64-char set. 
* These char-sets are usually alphabet in uppercase and lowercase.
* We can use some `online decode` like the one [here](https://www.base64decode.org/) or we can easily decode this text via terminal. 
* The command I use in terminal: 

``` 
root@busra:~$ echo "RWFjaCBCYXNlNjQgZGlnaXQgcmVwcmVzZW50cyBleGFjdGx5IDYgYml0cyBvZiBkYXRhLg==" | base64 -d
```

![image](https://user-images.githubusercontent.com/62840507/129718197-c45bd25b-a945-4c86-af37-dc053f24b22a.png)


**Solution :** Each Base64 digit represents exactly 6 bits of data.


#####  5. Hex String
```
68 65 78 61 64 65 63 69 6d 61 6c 20 6f 72 20 62 61 73 65 31 36 3f
```

* This encryption has two different names: hex and base16. 
* The way you can tell it’s in hex is the spacing between each couplet and the character set, that is 0–9 then a-f, adding to 16.
* We can use some `online decode` like the one [here](https://www.rapidtables.com/convert/number/hex-to-ascii.html) or we can easily decode this text via terminal. 
* We convert lowercase hex to ASCII using xxd. We combine the options -p and -r together for xxd and we can get the ASCII string.
* The command I use in terminal:

``` 
root@busra:~$ echo "68 65 78 61 64 65 63 69 6d 61 6c 20 6f 72 20 62 61 73 65 31 36 3f" | xxd -r -p
```
![image](https://user-images.githubusercontent.com/62840507/129718781-7d1cb7e2-5823-494c-9d87-366ea689bd57.png)

**Solution :** hexadecimal or base16?


#####  6. ROT13
```
Ebgngr zr 13 cynprf!
```

* This password is more complex like rot13, but special characters are also involved. 
* Rot 13 or known as rotate 13 is a form of Caesar cipher which rotate in 13 times.
* We can do the solution [online.](https://rot13.com/). 

**Solution :** Rotate me 13 places!


#####  7. Rot 47
```
*@F DA:? >6 C:89E C@F?5 323J C:89E C@F?5 Wcf E:>6DX
```

* Rot 47 or known as rotate 47 is another form of Caesar cipher which rotate in 47 times.
* We can do the solution [online.](https://www.dcode.fr/rot-47-cipher).

**Solution :** You spin me right round baby right round (47 times)

#####  8. Morse Code
```
- . .-.. . -.-. --- -- -- ..- -. .. -.-. .- - .. --- -.

. -. -.-. --- -.. .. -. --.

```

* Morse code is a combination of signal made of short and long impulsion (dot and dash). 
* It was designed for telecommunication.
* In the eighth question, there is a text encrypted with morse code. 
* The solution can be done [online.](http://www.unit-conversion.info/texttools/morse-code/) 

**Solution :** telecommunication ecoding 


#####  9. BCD to ASCII
```
85 110 112 97 99 107 32 116 104 105 115 32 66 67 68
```

* This type of encryption is BCD.
* We can solve this encryption type by looking at the ASCII table, or we can do this with [online](https://www.rapidtables.com/convert/number/ascii-hex-bin-dec-converter.html) tools.
 
**Solution :** Unpack this BCD


#####  10. Multiple cipher

```
```

* In the tenth question, a very long ciphertext is given. 
* In deciphering this text, we will decrypt several different encryptions in a few steps.
* 
**Solution :** 


### [Task 2] Spectrograms 

* A spectrogram is a visual representation of the spectrum of frequencies of a signal as it varies with time. When applied to an audio signal, spectrograms are sometimes called sonographs, voiceprints, or voicegrams. When the data is represented in a 3D plot they may be called waterfalls.
* I used the Sonic Visualizer application for this solution. 

![Spectrograms](https://user-images.githubusercontent.com/62840507/130035670-bfe64654-96e5-4175-a34c-16fe0083288a.png)


**Solution :** Super Secret Message


### [Task 3] Spectrograms 

* Steganography is the practice of concealing a file, message, image, or video within another file, message, image, or video.

* In this task we are given a photo and we will use the steghide tool to find the hidden txt in this photo. 
* --extract: extract, output data 
* -sf: –stegofile, hidden data 

* The command I use for this task:

```
root@busra:~$ steghide --extract -sf stegosteg.jpg 
```

![image](https://user-images.githubusercontent.com/62840507/130039106-9c076582-8148-4748-92dd-5cf460628202.png)


* Extracted the data to a file named steganopayload2248.txt. We can open it with the cat command and read it. We don't need to type anything with a null character password.
* This task can also be solved with an [online](https://futureboy.us/stegano/decinput.html) tool. 


**Solution :** SpaghettiSteg


### [Task 4]  Security through obscurity 

* Security through obscurity is the reliance in security engineering on the secrecy of the design or implementation as the main method of providing security for a system or component of a system.
* The strings command allows you to see the Alphabetically meaningful character groups contained in these binary files. That's why we look at the values with the strings command. This way we find both flags as plain text. 


![image](https://user-images.githubusercontent.com/62840507/130041365-887ae856-298b-42e9-bb2f-deac316598e0.png)

* This task can also be solved with an [online](https://29a.ch/photo-forensics/#forensic-magnifier) tool.

![image](https://user-images.githubusercontent.com/62840507/130042440-1722e52f-3661-428c-a579-a40f432ef082.png)


#####  1. Download and get 'inside' the file. What is the first filename & extension?

* The command I use for this task:
```
root@busra:~$ strings meme.jpg
```

**Solution :** hackerchat.png


#####  2. Get inside the archive and inspect the file carefully. Find the hidden text.

**Solution :** AHH_YOU_FOUND_ME!
