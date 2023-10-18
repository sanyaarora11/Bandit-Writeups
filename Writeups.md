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
In the next level it is mentioned that the password is stored in a file called <b>-</b> located in home directory. After logging in level 1 I ran the <b>ls</b> command and the output showed me <b>-</b> file. However it did not directly worked with <b>cat</b> command as in previous case. So, using the information under <b>find</b> command in the manual page :
<b>if a path argument would start with a `-', then find would treat
       it as expression argument instead.  Thus, to ensure that all
       start points are taken as such, and especially to prevent that
       wildcard patterns expanded by the calling shell are not
       mistakenly treated as expression arguments, it is generally safer
       to prefix wildcards or dubious path names with either `./' or to
       use absolute path names starting with '/'.</b> , the output gave a string which is the password for the next level.

       

       

