# Crack the Hash :octocat:

* We can use ` hash-identifier `  to find the hashing algorithm.
* Hashcat is a CLI password cracker that can be used in multiple platforms, which supports decryption on different hash types.
```hashcat -a <attack_mode> -m <hash_type> [path_to_hash_file] [path_to_dict_file]```

### [Task 1] Level 1


######  1. MD5
* Hash : 48bb6e862e54f2a795ffc4e541caed4d** 

* Hint : MD5

``` root@busra:~$ hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : easy*

######  2. SHA-1
* Hash : CBFDAC6008F9CAB4083784CBD1874F76618D2A97** 

* Hint : Sha.. but which version 

``` root@busra:~$ hashcat -m 100 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : password123*

######  3. SHA-256
* Hash : 1C8BFE8F801D79745C4631D09FFF36C82AA37FC4CCE4FC946683D7B336B63032** 

* Hint : sha..

``` root@busra:~$ hashcat -m 1400 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : letmein*

######  4. BCrypt 
* Hash : $2y$12$Dwt1BZj6pcyc3Dy1FWZ5ieeUznr71EeNkJkUlypTsgbX1H68wsRom** 

* Hint : bcrypt

At the beginning of the hashed value, we can see the `$2y$`, this is a hash signature and we can Google what hashing algorithm has this signature. We can find out that this is hashed using the bcrypt hashing algorithm. Again that password can be cracked using mode `-m 3200` in hashcat but it might take a lot of time. So, we can look up for some `online bcrypt cracking tools` like the one [here](https://www.onlinehashcrack.com/). We'll get the desired cracked value.

*Solution : bleh*

######  5. MD4 
* Hash : 279412f945939ba78ce0758d3fd83daa** 

* Hint : MD4

``` root@busra:~$ hashcat -m 900 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : Eternity22*
