# Writeups

## Level 0
I used <b>ssh</b> command to log in to bandit0. <br> They have given username (bandit0) and password (bandit0) and port 2220.
<br>
It is required to find <b>password for bandit1</b> using it.

## Level 1
### Level 0 -> Level 1
I took help from the manual pages and walkthrough playist to clear this level. <br> While logged into the Level0 I used <b>ls</b> command to see the files. After running the <b>ls</b> command, the output showed that there is a file named <b>readme</b> . Then I used <b>cat readme</b> to read the file and it contained a string which I used as the password to log in to bandit1.

![bandit](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/2e9deb7c-81cb-41eb-89c3-31fd350d6b49)
<br>
username bandit1
<br>
password NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL

![Screenshot (6)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/91c07183-7f2c-4cb1-bf27-292dd4898821)

<br>

## Level 2
### Level 1 -> Level 2
In the next level it is mentioned that the password is stored in a file called <b>-</b> located in home directory. After logging in level 1 I ran the <b>ls</b> command and the output showed me <b>-</b> file. However it did not directly worked with <b>cat</b> command as in previous case. So, using the information under <b>find</b> command in the manual page : <b>if a path argument would start with a `-', then find would treat it as expression argument instead.  Thus, to ensure that all start points are taken as such, and especially to prevent that  wildcard patterns expanded by the calling shell are not mistakenly treated as expression arguments, it is generally safer to prefix wildcards or dubious path names with either `./' or to  use absolute path names starting with '/'.</b> , the output gave a string which is the password for the next level. 

![Screenshot (9)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/26df7c7d-c4ba-4224-b3cf-dab0a37ce7e8)

<br>
username bandit2
<br>
password rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi


## Level 3
### Level 2 -> Level 3
The password for the next level is stored in a file called spaces in this filename. After running <b>ls</b> command, the output gave the name of the file <b>spaces in this filename</b> . To handle spaces in file names we can use forward slash(\) or double quotes ("") with the file name.
<br>
When I ran the <b>cat</b> command with the filename in double quotes it printed the output which is the password for the next level.

![Screenshot (10)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/5232d220-b19a-4703-902c-9acb2151b3a8)

<br>
username bandit3
<br>
password aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG


## Level 4
### Level 3 -> Level 4
While logged in the level 3 I ran the <b>ls</b> command as it is writtent that the password is in a hidden file in the <b>inhere</b> directory. To move into the inhere folder I used <b>cd</b> command. Then I ran the <b>ls -al</b> command to see all the files. <b>-a</b> command is used to see files starting with dot , i.e. , hidden files. The output gave a hidden file <b>.hidden</b> and after running the <b>cat .hidden</b> command the output gave a string which is the password for the next level. Using ssh command I logged in to the next level.

![Screenshot (13)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/421070e3-d787-4d47-bc69-8d9795602c19)

<br>
username bandit4
<br>
password 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe


