## Level 2 &rarr; 3: Escaping Spaces
#### Goal: 
- Find the password in a file named ``` spaces in this filename. ```
  
### Method:
  - 1. Files with spaces require the spaces to be escaped so the shell treats the entire name as a single argument
  - 2. Used single quotes ```('')``` before typing the filename to escape it. Alternatively, putting a slash before each word in the file would also work.
    
### Key Concept:
- Using single quotes ```('')``` for escaping characters or single/double quotes for literal strings in the shell.
  
#### Command Used: 
``` bandit2@bandit:~$ cat "spaces in this filename" or cat spaces\ in\ this\ filename```

### Successfully Acquired 

Password: ```xxxxx```

Next Login Command:
``` ssh bandit3@bandit.org.overthewire.org -p 2220```
