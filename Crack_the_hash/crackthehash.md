# Crack the Hash :octocat:

* We can use ` hash-identifier `  to find the hashing algorithm.
* Hashcat is a CLI password cracker that can be used in multiple platforms, which supports decryption on different hash types.
```hashcat -a <attack_mode> -m <hash_type> [path_to_hash_file] [path_to_dict_file]```

### [Task 1] Level 1


######  1. 
* Hash : 48bb6e862e54f2a795ffc4e541caed4d** 

* Hint : MD5

``` root@busra:~$ hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : easy*

######  2. 
* Hash : CBFDAC6008F9CAB4083784CBD1874F76618D2A97** 

* Hint : Sha.. but which version

``` root@busra:~$ hashcat -m 100 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : password123*

######  1. 
* Hash : 48bb6e862e54f2a795ffc4e541caed4d** 

* Hint : MD5

``` root@busra:~$ hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : easy*

######  1. 
* Hash : 48bb6e862e54f2a795ffc4e541caed4d** 

* Hint : MD5

``` root@busra:~$ hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : easy*

######  1. 
* Hash : 48bb6e862e54f2a795ffc4e541caed4d** 

* Hint : MD5

``` root@busra:~$ hashcat -m 0 hash.txt /usr/share/wordlists/rockyou.txt --force```


*Solution : easy*
