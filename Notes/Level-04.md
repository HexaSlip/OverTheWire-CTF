## Level 4 to 5: Identifying Human-Readable Files (file)
Goal: The password is in the only human-readable file in the inhere directory
Method:
  1. The directory contained multiple files (-file00 through -file09) that were not obviously text files.
  2. Used the file command with a wildcard pattern (./-file*) to check the content type of all files at once.
  3. Identified the one files designated as ASCII text (human-readable) and used cat to read its contents. 
Key Concept: Using the file command to determine the content type of a file (e.g., ASCII text, data, binary)
Commands Used:
bandit4@bandit:~/inhere$ file ./-file*
bandit4@bandit:~/inhere$ cat ./-file07
Sucessfully acquired the password, logged out of the server, and entered into level 6 using the discovered password. 

