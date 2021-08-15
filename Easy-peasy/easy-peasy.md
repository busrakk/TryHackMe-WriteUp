# Easy Peasy :octocat:

### [Task 1]


#####  1. How many ports are open?
* Scan open port 
* -sV : Version detection
* -p- : All ports to scan

```root@busra:~$ nmap -p- -sV 10.10.194.164```
```
PORT      STATE SERVICE VERSION
80/tcp    open  http    nginx 1.16.1
6498/tcp  open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
65524/tcp open  http    Apache httpd 2.4.43 ((Ubuntu))
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

```


**Solution : ** 3 


#####  2. What is the version of nginx?

**Solution :** 1.16.1


#####  3. What is running on the highest port?

**Solution :** Apache


### [Task 2]


#####  1. Using GoBuster, find flag 1.
* Gobuster allows us to find hidden web directories running on port 80.
* -u : URL
* -w : Wordlist

```root@busra:~$ gobuster dir -u 10.10.194.164 -w /usr/share/dirb/wordlists/common.txt```

* The result is as follows:
```
/hidden               (Status: 301) [Size: 169] [--> http://10.10.194.164/hidden/]
/index.html           (Status: 200) [Size: 612]                                   
/robots.txt           (Status: 200) [Size: 43]                                    

```

* We have a directory /hidden to check out as well as robots.txt file is also available for having a look
* When we visit the /hidden directory, we see nothing but an image. “View source” gets us no further… 
* Look into ```/hidden``` directory we discovered in gobuster.

```root@busra:~$ gobuster dir --url http://10.10.194.164/hidden --wordlist /usr/share/dirb/wordlists/common.txt ```

```
/index.html           (Status: 200) [Size: 390]
/whatever             (Status: 301) [Size: 169] [--> http://10.10.194.164/hidden/whatever/]

```
