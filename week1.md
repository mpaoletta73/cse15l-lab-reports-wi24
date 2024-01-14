# Command `cd`
## 1. `cd` Example With No Arguments
Input: `[user@sahara ~]$ cd` <br/>
Output: `[user@sahara ~]$ ` <br/>
At this point, the working directory was /home <br/>
This command requires the name of a file or folder so that it can change the current directory.  <br/>
The terminal thinks that the file that you are trying to find is just the basic /home so it keeps the directory the same. <br/>
This output is not an error since you are just trying to change the directory back to the original directory. <br/>
## 2. `cd` Example With Path To Directory
Input: `[user@sahara ~]$ cd lecture1`<br/>
Output: `[user@sahara ~/lecture1]$ ` <br/>
Originally, the working directory was /home, but for the output it changed to /home/lecture1 <br/>
With a folder name, it changes the directory so that it includes the folder, and now the directory includes the folder. <br/>
This output is not an error since it allows you to access that directory from that point. <br/>
## 3. `cd` Example With Path To File <br/>
Input: `[user@sahara ~/lecture1]$ cd Hello.Java` <br/>
Output: `bash: cd: Hello.java: Not a directory` <br/>
The working directory was /home/lecture1 and if it wasn't it wouldn't have been able to access a file name and there would have been an error message. <br/>
Due to the file name being in the folder, it could access it but since the file isn't a directory it prints out an error message. <br/>
This was an error message due to typing a file name instead of a directory name. <br/>
---
# Command `ls`
## 1. `ls` Example With No Arguments
Input: `[user@sahara ~]$ ls` <br/>
Output: `lecture1` <br/>
At this point, the working directory was and still is /home <br/>
The output here tells you the current directories and files that you can view by using the cd function. <br/>
This output is also bolded which tells me that "lecture1" is a directory and not a file name. <br/>
This output is not an error as it is giving useful information. <br/>
## 2. `ls` Example With Path To Directory
Input: `[user@sahara ~]$ ls lecture1` <br/>
Output: `Hello.java messages README` <br/>
At this point, the working directory was and still is /home <br/>
The output here tells you the current directories and files that you can view if you change the directory to /home/lecture1. <br/>
This allows the user to view a file without changing the current directory to check the contents of the directory. <br/>
This output is not an error as it is giving useful information. <br/>
## 3. `ls` Example With Path to File
Input: `[user@sahara ~/lecture1]$ ls Hello.java` <br/>
Output: `Hello.java` <br/>
For this one, I changed the working directory to /home/lecture1 so that I could try typing a file. <br/>
The output here is a little confusing at first but makes sense if you think of what you are asking the computer to tell you. <br/>
You're effectively asking the computer to tell you what could be in the file that is just a text file so the computer just responds with the name of the file. <br/>
This output doesn't give a major error since you are giving a file that is contained in the current directory, but the information that it provides is essentially useless. <br/>
---
# Command `cat`
## 1. `cat` Example With No Arguments
<br>
## 2. `cat` Example With Path To Directory
<br>
## 3. `cat` Example With Path To File
<br>
---

