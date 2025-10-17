## Level 5 &rarr; 6: File Searching with ```grep``` and Regex 
#### Goal
The challenge required locating a single, human-readable file buried deep within a complex structure of directories and binary/non-text files. The file was defined by three specific attributes: __human,readable, 1033 bytes in size,__ and __non executable.__

### The Efficient Solution
The solution involved using the powerful and precise ```find``` command to filter the file system based on these criteria.

| Component       | Meaning        | What it Does  |
| :-----------    | :------------: | ------------: |
| ```find .```    | Search Start   | Begins the search in the current directory (```.```) and recursively searches all subdirectories|
| ```-type f```   | Type Filter    | Restricts the search results only to __regular files__ (excludes directories, links,etc).|
| ```-size 1033c```| Size Filter | Targets only files that are __exactly 1033 bytes__ fin size (the ```c``` specifies size in bytes).|
| ```! -executable```| Permission Filter| Uses the __negation operator__ (```!```) to __exclude__ all files that have the executable permission set.|

#### Command Used:
``` bandit5@bandit:~$ find . -type f -size 1033c ! -executable ```

#### Final Step (to get the password):
``` bandit5@bandit:~$ cat [filename found above]``` 

#### Successfully Acquired 
#### Password: 
```xxxxx```
#### Next Login Command:
``` ssh bandit6bandit.labs.overthewire.org -p 2220 ```
