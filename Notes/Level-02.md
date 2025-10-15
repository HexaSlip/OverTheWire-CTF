## Level 2 to 3: Escaping Spaces
Goal: Find the password in a file named spaces in this filename
Method:
  1. Files with spaces require the spaces to be escaped so the shell treats the entire name as a single argument
  2. Used a quotes before typing the filename to escape it. Alternatively putting a slash before each word in the file would also work. 
Key Concept: Using quotes for escaping character or single/double quotes for literal strings in the shell.
Command Used: 
bandit2@bandit:~$ cat "spaces in this filename" 
# Alternative: cat spaces\ in\ this\ filename
Sucessfully found the password, logged out of the server, and entered the password for Level 3.

