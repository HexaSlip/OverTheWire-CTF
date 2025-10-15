## Level 5 to 6: File Searching with grep and Regex 
This challenge required finding a specific file based on its properities( human-readable, 1033 bytes, not executable).
However, a much more efficient method is to search directly for the password pattern itself, which is a 32-character string of letters and numbers.

The Efficient Solution
Instead of relying on file metadata(size, permissions), I used a recursive grep search, piped the results, and extratcted the very first match
  Component:
grep -RhoE

  Meaning:
Recursive, No Filename, Only Match, Extended Regex

What it Does:
Searches all files under the current directory (.), extracts only the matching password string, and does not print the filename.

Component:
'[A-Za-z0-9]{32,}' 

Meaning:
Regex Pattern

What it Does:
Specifies that the search should start in the inhere directory.

Component:
**

Meaning:
head -n1'**

What it Does:
Piped Output

Command Used:
bandit5@bandit:~$ grep -RhoE '[A-Za-z0-9]{32,}' inhere | head -n 1

Successfully acquired the password for next level, logged out of server, and entered into Level 6. 
