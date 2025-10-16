## Level 1 &rarr; 2: Escaping the Hyphen (```-```)
#### Goal: 
- Find the password in a file named ```-```.
### Method:
 - 1. Attempting ```cat -``` failed because the hyphen (```-```) is interpreted as a __flag__ (option) for the ``` cat``` command, not a filename
 - 2. The solution was to use ```./``` to explicitly tell the shell that the path starts in the current directory, treating the hyphen as part of the file name
  
### Key Concept: 
- Preventing a shell from misinterpreting special characters(like the hyphen) by using ```./``` or the double-hyphen flag (```--```)
  
#### Command Used:
  ```bandit1@bandit:~$ cat ./-```
  
#### Successfully Acquired: 
#### Password: ```xxxxx```
#### Next Login Command:
```ssh bandit2bandit.labs.overthewire.org -p 2220 ```
