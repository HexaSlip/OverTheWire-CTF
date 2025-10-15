## Level 3 to 4: Hidden Files (ls -a)
Goal: The password is in a hidden file inside the inhere directory
Method:
  1. Navigated into the inhere directory using cd
  2. Used ls -a (the all flag) to show files starting with a dot (.), which are hidden in Linux.
  3. Used cat on the hidden file (.hidden) to retrieve hidden files and directories.
Commands Used:
  bandit3@bandit:~$ cd inhere
  bandit3@bandit:~/inhere$ ls -a
  bandit3@bandit:~/inhere$ cat.hidden
Sucessfully acquired the password, logged out of server, and used password to enter into Level 4

