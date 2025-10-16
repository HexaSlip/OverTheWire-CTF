## Level 0 &rarr; 1: Introduction to SSH and ```cat```

#### Goal: 
- Log in via SSH and find the password in a file named ```readme```.
### Method:
- 1. Used the ```ssh``` command with the provided username, host, and port.
- 2. Once logged in, I used ```ls``` to list files, revealing ```readme```.
- 3. Used the ```cat``` command to display the contents of the readme file.
	
### Key Concept:
Basic ```ssh``` syntax and the ```cat``` command for displaying file contents. 
#### Command Used:
	bandit0@bandit:~$ ls
	bandit0@banidt:~$ cat readme
#### Successfully Acquired:
#### Password: 
```xxxxx```
#### Next Login Command: 
```ssh bandit1@bandit.labs.overthewire.org -p 2220```
