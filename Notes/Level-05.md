## Level 5 &rarr; 6: File Searching with grep and Regex 
#### Goal
The password for the next level is stored in a file somewhere under the ```inhere``` directory and has all of the following properties: __human-readable, 1033 bytes in size__, and __not executable.__ 
### The Efficient Solution
Instead of relying on file metadata(size, permissions), I used a recursive ```grep``` search, piped the results, and extracted the very first match
| Component       | Meaning        | What it Does  |
| :-----------    | :------------: | ------------: |
| ```grep -RhoE```| Recursive, No Filename, Only Match, Extended Regex| Searches all files under the current directory (```.```), extracts _only_ the matching password string, and does not print the filename|
| ```'A-Za-z0-9]{32,}```| Regex Pattern  | Targets string of 32 or more alphanumeric characters, which is the exact format of the Bandit passwords. |
| ```inhere```          | Search Location| Specifies that the search should start in the ```inhere``` directory |
| **`             | head -n1' **   | Piped Output|

#### Command Used:
``` bandit5@bandit:~$ grep -RhoE '[A-Za-z0-9]{32,}' inhere | head -n 1 ```

#### Successfully Acquired 
#### Password: 
```xxxxx```
#### Next Login Command:
``` ssh bandit6bandit.labs.overthewire.org -p 2220 ```
