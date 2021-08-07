# Crack the Hash :octocat:

* We can use ` hash-identifier `  to find the hashing algorithm.
* Hashcat is a CLI password cracker that can be used in multiple platforms, which supports decryption on different hash types.

```hashcat -a <attack_mode> -m <hash_type> [path_to_hash_file] [path_to_dict_file]```

### [Task 1] Level 1


#####  1. MD5
* Hash : 48bb6e862e54f2a795ffc4e541caed4d

* Hint : MD5

``` root@busra:~$ hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt --force```


**Solution :** easy



#####  2. SHA-1
* Hash : CBFDAC6008F9CAB4083784CBD1874F76618D2A97

* Hint : Sha.. but which version 

``` root@busra:~$ hashcat -m 100 hash.txt /usr/share/wordlists/rockyou.txt --force```


**Solution :** password123



#####  3. SHA-256
* Hash : 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032 

* Hint : sha..

``` root@busra:~$ hashcat -m 1400 hash.txt /usr/share/wordlists/rockyou.txt --force```


**Solution :** letmein



#####  4. BCrypt 
* Hash : $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom 

* Hint : bcrypt

At the beginning of the hashed value, we can see the `$2y$`, this is a hash signature and we can Google what hashing algorithm has this signature. We can find out that this is hashed using the bcrypt hashing algorithm. Again that password can be cracked using mode `-m 3200` in hashcat but it might take a lot of time. So, we can use some `online bcrypt cracking tools` like the one [here](https://www.onlinehashcrack.com/). As a result we'll get the desired cracked value.

**Solution :** bleh



#####  5. MD4
* Hash : 279412f945939ba78ce0758d3fd83daa 

* Hint : MD4

With hashcat, we can figure out that this hash appears to be MD5 but when we try to crack this hash with hashcat using the mode -m 0, the hash does not get cracked. So, we can use another online hash cracker over [here](https://www.onlinehashcrack.com/) and get the cracked hash value.


**Solution :** Eternity22



### [Task 2] Level 2



#####  1. SHA-256 
* Hash : F09EDCB1FCEFC6DFB23DC3505A882655FF77375ED8AA2D1C13F640FCCC2D0C85

* Hint : SHA-256 

``` root@busra:~$ hashcat -m 1400 hash.txt /usr/share/wordlists/rockyou.txt --force```

**Solution :** paule




#####  2. NTLM 
* Hash : 1DFECA0C002AE40B8619ECF94819CC1B

* Hint : NTLM
* NTLM hashes can be cracked with hashcat using mode ``` -m 1000.```

``` root@busra:~$ hashcat -m 1000 hash.txt /usr/share/wordlists/rockyou.txt --force```

**Solution :** n63umy8lkf4i




#####  3. SHA-512, $6$ Salted Hash 
* Hash : $6$aReallyHardSalt$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02.

* Salt: aReallyHardSalt

We can crack this hash using mode ```-m 1800 ``` in hashcat.

``` root@busra:~$ hashcat -m 1800 "\$6\$aReallyHardSalt\$6WKUTqzq.UQQmrm0p/T7MPpMbGNnzXPMAXi4bJMl9be.cfi3/qxIf.hsGpS41BqMhSrHVXgMpdjS6xeKZAs02." /usr/share/wordlists/rockyou.txt ```

**Solution :** waka99




#####  4. HMAC-SHA1 
* Hash : e5d8870e5bdd26602cab8dbe07a942c8669e56d6

* Salt: tryhackme

* Hint : HMAC-SHA1 


We know that we are provided both the hash and salt. it must be by some way passed to the cracker in order to crack it in a proper way. So to do that there are two method:
   ``` <password>:<hash> ```
   ``` <hash>:<password> ```

* HMAC-SHA1 (key=$salt) hashes can be cracked with hashcat using mode ``` -m 160.```

``` root@busra:~$ hashcat -m 160 hash.txt /usr/share/wordlists/rockyou.txt ```

**Solution :** 481616481616
