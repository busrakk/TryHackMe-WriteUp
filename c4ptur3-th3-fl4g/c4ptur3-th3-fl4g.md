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

``` root@busra:~$ echo "MJQXGZJTGIQGS4ZAON2XAZLSEBRW63LNN5XCA2LOEBBVIRRHOM======" | base32 -d```

![image](https://user-images.githubusercontent.com/62840507/129717449-6beac9f9-63f5-44a6-9c57-7d9536292b98.png)

**Solution :** base32 is super common in CTF's


#####  4. 
```
RWFjaCBCYXNlNjQgZGlnaXQgcmVwcmVzZW50cyBleGFjdGx5IDYgYml0cyBvZiBkYXRhLg==
```

**Solution :** Each Base64 digit represents exactly 6 bits of data.


#####  5. 
```
68 65 78 61 64 65 63 69 6d 61 6c 20 6f 72 20 62 61 73 65 31 36 3f
```

**Solution :** hexadecimal or base16?


#####  6. 
```
Ebgngr zr 13 cynprf!
```

**Solution :** Rotate me 13 places!


#####  7. 
```
*@F DA:? >6 C:89E C@F?5 323J C:89E C@F?5 Wcf E:>6DX
```

**Solution :** You spin me right round baby right round (47 times)

#####  8. 
```
- . .-.. . -.-. --- -- -- ..- -. .. -.-. .- - .. --- -.

. -. -.-. --- -.. .. -. --.

```

**Solution :** telecommunication ecoding 


#####  9. 
```
85 110 112 97 99 107 32 116 104 105 115 32 66 67 68
```

**Solution :** Unpack this BCD


#####  10. 
```
```

**Solution :** 
