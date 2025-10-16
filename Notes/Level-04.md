## Level 4 &rarr; 5: Identifying Human-Readable Files (file)
#### Goal: 
- The password is in the _only human-readable_ file in the ```inhere``` directory
### Method:
-  1. The directory contained multiple files (```-file00``` through ```-file09```) that were not obviously text files.
-  2. Used the ```file``` command with a wildcard pattern (```./-file*```) to check the content type of all files at once.
-  3. Identified the one file designated as ``` ASCII text``` (human-readable) and used cat to read its contents. 
### Key Concept:
Using the ```file``` command to determine the content type of a file (e.g., ASCII text, data, binary)

#### Commands Used:
```
bandit4@bandit:~/inhere$ file ./-file*
bandit4@bandit:~/inhere$ cat ./-file07
```
#### Successfully Acquired 
#### Password: 
```xxxxx```
#### Next Login Command: 
``` ssh bandit5@bandit.labs.overthwire.org -p 2220```
