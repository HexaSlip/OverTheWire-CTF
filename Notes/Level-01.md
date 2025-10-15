## Level 1 to 2: Escaping the Hyphen (-)
Goal: Find the password in a file named -
Method:
  1.Attempting cat - failed because the hyphen (-) is interpreted as a flag(option) for the cat command, not a filename
  2. The solution was to use ./ to explicitly tell the shell that the path starts in the current directory, treating the hyphen as part of the file name
Key Concept: Preventing a shell from misinterpreting special characters(like the hyphen) by using ./ or the double-hyphen flag (--)
Command Used:
  bandit1@bandit:~$ cat ./-
Sucessfully acquired the password, logged out of the server, and entered via SSH command into Level 2. 

