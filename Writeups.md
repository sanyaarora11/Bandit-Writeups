# OverTheWire - Bandit - Writeups

## Level 0
I used <b>ssh</b> command to log in to bandit0. <br> They have given username (bandit0) and password (bandit0) and port 2220.
<br>
It is required to find <b>password for bandit1</b> using it.

## Level 1
### Level 0 -> Level 1
I took help from the manual pages and walkthrough playist to clear this level. <br> While logged into the Level0, I used <b>ls</b> command to see the files. After running the <b>ls</b> command, the output showed that there is a file named <b>readme</b> . Then I used <b>cat readme</b> to read the file and it contained a string which I used as the password to log in to bandit1.
<br>
![bandit](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/2e9deb7c-81cb-41eb-89c3-31fd350d6b49)
<br>
username bandit1
<br>
password NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
<br>
![Screenshot (6)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/91c07183-7f2c-4cb1-bf27-292dd4898821)

<br>

## Level 2
### Level 1 -> Level 2
In the next level it is mentioned that the password is stored in a file called <b>-</b> located in home directory. After logging in level 1 I ran the <b>ls</b> command and the output showed me <b>-</b> file. However it did not directly worked with <b>cat</b> command as in previous case. So, using the information under <b>find</b> command in the manual page : <b>if a path argument would start with a '-', then find would treat it as expression argument instead.  Thus, to ensure that all start points are taken as such, and especially to prevent that  wildcard patterns expanded by the calling shell are not mistakenly treated as expression arguments, it is generally safer to prefix wildcards or dubious path names with either `./' or to  use absolute path names starting with '/'.</b> , the output gave a string which is the password for the next level. 
<br>
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
<br>
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


![Screenshot (15)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/6359d724-19a0-4df5-9b58-69c54c6c496d)


## Level 5
### Level 4 -> Level 5
The password for next level is in a human-readable file in inhere directory. I used the <b>ls</b> command and then <b>cd</b> command to get inside inhere folder. I used <b>ls -a</b> command , it did not work. However, after going through playlist and manual pages, using <b>file ./*</b> command as <b>file</b> gives information about any file passed as a parameter, human-readable file is seen clearly.
 <br>
 Executing the command <b>cat ./-file</b> , the output gave a string which is the password for the next level. 

 ![Screenshot (16)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/1d2d9cac-1023-4108-948a-fcb530eff64c)

 <br>
 username bandit5
 <br>
 password lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

 ![Screenshot (18)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/ba6f9371-8128-4d89-8da2-49817a0657d9)

 ## Level 6
 ### Level 5 -> Level 6
 I ran the <b>ls</b> command to check for the directory. Then I ran the <b>cd</b> command to go into <b>inhere</b> directory and then again ran the <b>ls</b> command to see all the files. In order to find out the exact file with the properties given I used the manual pages for the <b>find</b> command. 

![Screenshot (20)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/2c2928c7-f7db-4d6f-9ec1-d84b483e4da1)
![Screenshot (21)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/87104b5c-f4b9-497c-8b7c-113eac392966)
![Screenshot (22)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/e59a21aa-25b2-4cc5-a772-0b7179ecd884)

<br>
With the help of these and some help from walkthrough playlist I ran <b>find</b> command and the output gave a file and using <b>cat</b> command a string appeared which is the password for the next level. 

![Screenshot (25)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/969b86f9-01ce-4b08-b5eb-848907a81bfb)

<br>
username bandit6
<br>
password P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Level 7
### Level 6 -> Level 7
I used the <b>ls</b> command but it did not give any output. Then I used <b> man find</b> command and under that i searched for <b>/user</b> , <b>/group</b> and <b>/size</b> and with help of these I tried to write a command using <b>find /</b>, as it is located somewhere in the server, so we need to find in the root directory. After running the command it did gave an output that had the name of the file in which contained the password but it also gave some error files.

![Screenshot (30)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/19b7d913-9241-4ab0-b00a-7567ceaef2f9)

To rectify it I took help from the walkthrough playlist and then used <b>2>/dev/null</b> to redirect the error messages to null so that they do not show on the standard output. The output is the name of the file. I read the file with help of <b>cat</b> command and the output gave the string which is the password for the next level.

![Screenshot (31)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/3f54ea00-a4f2-4f1c-866e-3e05b5072aef)

<br>
username bandit7
<br>
password z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S

## Level 8
### Level 7 -> Level 8
I ran the <b>ls</b> command and it gave the name of a file which when I read using <b>cat</b> command produced a bunch of lines  and it looked like all of the lines had the same structure. It was a word followed by some spaces and then a possible password. Since, The hint was that the password is next to the word millionth I used <b>cat</b> command with another command <b>grep</b>. 

![Screenshot (32)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/ec022fe7-b4ef-4239-89b5-e0b97026ade8)

<br>
The output gave one line as output which had the password for the next level.

![Screenshot (33)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/0c18c8a4-1f73-4871-a95f-ed58c28f4eb6)

<br>
username bandit8
<br>
password TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Level 9
### Level 8 -> Level 9
I ran the <b>ls</b> command and the name of the file appeared. Since, it is given that the password  is the only line of text that occurs only once, it is needed to remove the duplicates. I looked for <b>sort</b> and <b>uniq</b> commands in the manual page and use google to know how they are used. 

![Screenshot (36)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/1b58c47c-b5f1-40e5-ba4e-44f63f02d34e)
![Screenshot (37)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/76d7ceaa-7730-45e0-8b66-a5840d5d79bf)

<br>
The command produced the output which is the password for the next level.

![Screenshot (38)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/90a194b5-4bd3-4b59-a17c-7167c7375f2c)

<br>
username bandit9
<br>
password EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## Level 10
### Level 9 -> Level 10
The password for the next level is stored in the file <b>data.txt</b> in one of the few human-readable strings which means the file contains both strings which is readable by humans and binary data which is not readable by humans. So, looking under <b>strings</b> section in the manual and with some help of walkthrough playlist , I ran a command to see all the strings that started with <b>"="</b> sign. According to the pattern followed ine of them is the password for the next level.

![Screenshot (39)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/8b3bcf32-428a-45f5-9549-3e46171fb225)
![Screenshot (40)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/72a98e6e-3eca-43ca-a1f7-8b4fe8155d85)

<br>
username bandit10
<br>
password G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s

## Level 11
### Level 10 -> level 11
The password for the next level is stored in the file data.txt, which contains base64 encoded data, so I checked for the <b>base64</b> in the manual page and using <b>--decode</b> command , the output gave the password for the next level. 

![Screenshot (41)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/8dcaaf16-b7d4-473b-9c26-a1770f8a9f1c)

<br>
username bandit11
<br>
password 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM

## Level 12
### Level 11 -> Level 12
The uppercase and lowercaseletters in the password have been rotated by 13 positions. In order to get the correct password each letter has to be replaced by the letter 13 positions ahead. I read about <b>rot13</b> on net gone through manual pages of <b>tr</b> command. The use of <b>tr</b> command was bit difficult to undersatand so directly after using <b>ls</b> and <b>cat</b> command I tried replacing every letter in the string produced by <b>cat data.txt</b> to a 13 positions ahead letter. It worked as it was the password for the next level.

![Screenshot (42)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/2a53c374-5724-4663-a1da-14505c2bb513)
![Screenshot (43)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/e62dcdf7-c922-4bde-820a-cd3b63f51618)
![Screenshot (44)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/f5e62d66-42d7-4214-b519-ee481cb45f20)

<br>
username bandit12
<br>
password WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi after decrypting JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv

## Level 13
### Level 12 -> Level 13
This is so far the most difficult level for me as even after going through manual pages, walkthrough playlist and google search, I faced a lot of confusion to clear the level after committing a lot of errors. Uncompressing the files repeatedly was a bit tedious but keeoing manual page and walkthrough playlist handy has a helped alot. First of all as it is mentioned I have to create a directory using <b>mkdir</b> command. So, for this I went through its manual page and created a folder with the name <b>word</b>.

![Screenshot (45)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/c032f73c-1f58-4385-9603-c62df99dc167)

<br>
After making directory I copied the <b>data.txt</b> file to the folder using <b>cp</b> command.

![Screenshot (46)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/8221b297-a0ce-4f90-8e79-e09607d1e2fa)

<br>
After this I used <b>cd</b> command to change the working directory. After running <b>cat data.txt</b> command a hexdump file appeared. In order to decypher hexdump of the file I used <b>xxd -reverse data.txt > changes</b>, to reverse the hexdump and save it to a file with name <b>changes</b>.

![Screenshot (48)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/74828f2a-1bdc-4e48-a698-304eede17d20)

<br>
After this I used the <b>file</b> command to know the type of the file. It showed that the file was <b>gzip</b> compressed. So, I through manual pages of <b>gzip</b> command.

![Screenshot (52)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/1c70824a-dd08-423e-a28b-4db75362a5aa)

<br>
Then I ran the command <b>gunzip changes</b> , it produced the output <b>gzip: changes: unknown suffix -- ignored</b>, then again I ran the command <b>mv changes changes.gzip</b> with the use of <b>mv</b> and then again <b>gunzip changes.gzip</b> which gave the output <b>gzip: changes.gzip: unknown suffix -- ignored</b>.

![Screenshot (47)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/8fa8e2d4-38c4-4409-8682-12a25d342e30)

<br>
Then I used <b>mv</b> command and changed the extension to <b>.gz</b>. After this I tried to decompress it and used the <b>file</b> command to know the type of file. The file is compressed with <b>bzip2</b>. I read about the <b>bzip</b> command in the manual page.

![Screenshot (53)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/28e95b20-06f2-4cfa-9a30-17e573ead93e)

<br>
Then I tried to uncompress it using <b> bunzip2 changes</b> which gave this output <b>bunzip2: Can't guess original name for changes -- using changes.out</b>. After this using <b>ls</b> and <b>file</b> commands the output showed that the file is compressed with <b>gzip</b>. I used the <b>.gz</b> extension , unzipped it and ran the <b>file changes command</b> which gave the following output <b>changes: POSIX tar archive (GNU)</b> which means the next compression was done with <b>tar</b>. I used the manual page for it.

![Screenshot (55)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/7b6130a0-3da9-4bfa-874c-672aecc407fc)

<br>
Using walkthrough playlist I ran the command <b>tar x changes</b> which gave the following output <b>tar: Refusing to read archive contents from terminal (missing -f option?) tar: Error is not recoverable: exiting now</b>. Then I ran <b>tar xf changes</b> and <b>ls</b> commands which gave gave a file named <b>data5.bin</b>. After running <b>file</b> command the output showed that the file was compressed with <b>tar</b>. So, I ran <b>tar xvf data5.bin</b> and <b>ls</b> commands and the output gave a file compressed with <b>bzip2</b>. Then the file was compressed with <b>tar</b> , so I used <b>tar xvf data6.bin.out</b> command which gave a file named <b>data8.bin</b>. Finally, the last layer of compression was done with <b>gzip</b> and after changing the extension and unzipping the file, the output gave <b>data8.bin</b> which has <b>ASCII text</b> and after using <b>cat</b> command the output gave the password for the next level.

![Screenshot (49)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/8dc70504-4172-40d6-840b-6206720262ea)
![Screenshot (50)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/5ce5376a-5cfe-47a2-97e8-d94519f5812d)
![Screenshot (51)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/63a3e1b1-9256-44c0-9ead-391a76fec0db)
![Screenshot (54)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/f220ad19-67cc-4abd-9068-d65b5df7d578)

<br>
Initially, I did some mistakes while typing commands but then I rectified it.

![Screenshot (56)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/13851ad1-72c9-4929-9a5d-9faaec82577f)
![Screenshot (57)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/a5488110-579f-44c1-ae2d-99509fd75e60)
![Screenshot (58)](https://github.com/sanyaarora11/Bandit-Writeups/assets/147926344/d2ea128e-6c6a-4077-ada1-bd3cbbe7aadb)

<br>
username bandit13
<br>
password wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw

## Level 14
### Level 13 -> Level 14
To clear this level we get a private <b>SSH</b> key that can be used to login into the next level. Initially I used walkthrough playlist to clear this level but it gave an error.
