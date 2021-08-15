# Easy Peasy :octocat:

### [Task 1]


#####  1. How many ports are open?
* Scan open port 

```root@busra:~$ nmap -p- -sS -sV 10.10.194.164```
```
PORT      STATE SERVICE VERSION
80/tcp    open  http    nginx 1.16.1
6498/tcp  open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
65524/tcp open  http    Apache httpd 2.4.43 ((Ubuntu))
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

```


**Solution : ** 3 


#####  2. What is the version of nginx?

``` root@busra:~$ ```


**Solution :** 1.16.1


#####  3. What is running on the highest port?

``` root@busra:~$ ```


**Solution :** Apache


### [Task 2]


#####  1. Using GoBuster, find flag 1.
* Gobuster allows us to find hidden web directories running on port 80.

```root@busra:~$ gobuster dir -u 10.10.194.164 -w /usr/share/dirb/wordlists/common.txt```

* The result is as follows:
```
/hidden               (Status: 301) [Size: 169] [--> http://10.10.194.164/hidden/]
/index.html           (Status: 200) [Size: 612]                                   
/robots.txt           (Status: 200) [Size: 43]                                    

```
