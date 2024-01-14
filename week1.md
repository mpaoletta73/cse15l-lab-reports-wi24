# Command `cd`
## 1. `cd` Example With No Arguments
Input: `[user@sahara ~]$ cd` 
Output: `[user@sahara ~]$ ` 
At this point, the working directory was /home 
This command requires the name of a file or folder so that it can change the current directory.  
The terminal thinks that the file that you are trying to find is just the basic /home so it keeps the directory the same. 
This output is not an error since you are just trying to change the directory back to the original directory. 
## 2. `cd` Example With Path To Directory
Input: `[user@sahara ~]$ cd lecture1`
Output: `[user@sahara ~/lecture1]$ ` 
Originally, the working directory was /home, but for the output it changed to /home/lecture1 
With a folder name, it changes the directory so that it includes the folder, and now the directory includes the folder. 
This output is not an error since it allows you to access that directory from that point. 
## 3. `cd` Example With Path To File
Input: `[user@sahara ~/lecture1]$ cd Hello.Java` 
Output: `bash: cd: Hello.java: Not a directory` <br>
The working directory was /home/lecture1 and if it wasn't it wouldn't have been able to access a file name and there would have been an error message. <br>
Due to the file name being in the folder, it could access it but since the file isn't a directory it prints out an error message. <br>
This was an error message due to typing a file name instead of a directory name. <br>
---
# Command `ls`
## 1. `ls` Example With No Arguments
<br>
## 2. `ls` Example With Path To Directory
<br>
## 3. `ls` Example With Path To File
<br>
---
# Command `cat`
## 1. `cat` Example With No Arguments
<br>
## 2. `cat` Example With Path To Directory
<br>
## 3. `cat` Example With Path To File
<br>
---

