<h1>File permissions in Linux</h1>

<h2>Project Description</h2>
In this project I will demonstrate file permission control and management through Linux CLI(command line interpreter), using bash shell.
<br />


<h2>Tools used</h2>

- <b>Linux OS</b> 

<h2>Check file and directory details:</h2>

<p align="center">
The first step is to enter the desired project directory with the cd(change directory) command.
After that, I list all the files, including the hidden ones with command: ls -la. ls to list files and -la to list the hidden ones, as the picture indicates. <br/>
<img src="https://i.imgur.com/Z1lbnfV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <h2>Describeing the permissions string</h2>
     <p align="center">
       -rw-rw-rw-  This permission string belongs to the “project_k.txt” file.
Permission strings give us information about what kind of permissions/rights a certain user or certain groups have with the given file.
Moving from the left to the right, the first hyphen means that this is a regular type file.
The first string always describes the file type which can be a hyphen(-) as regular or directory(d).
The next 9 characters indicate the permission for the user/group/others triple, in this sequence.
User=The owner of the file
Group=A larger network the user is in.
Others=All other users in the system.
Regarding permissions we also use 3 categories in the same sequence.
r=read
w=write
x=execute
If one of these 9 characters is a hyphen, it indicates that the given category has no permission to the given action.
Therefore, this given string can be read as the follow:
Regular file type, everyone can read, write in the file and nobody can execute with it.
<br />
<br />
<h2>Change file permissions:</h2>

   <p align="center">
    The company does not want others to have write access to any of the files.
Based on this I checked if any files have write permission for others.
Only projeckt_k.txt had so I proceeded to remove it, as the picture indicates.
<img src="https://i.imgur.com/MSE6kxL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  <h2>Change file permissions:</h2>
  <p align="center">
The company does not want .project_x.txt to be modifiable by anyone but it wants to be readable for the user and group. The file is archived, so it’s hidden. Hidden file names start with a dot( . ).
First I removed write permission from both the user and the group.
After that I gave read permission to the group, as the picture indicates. <br/>
<img src="https://i.imgur.com/JUTaCnd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <p align="center">
<br />
<br />
    <h2>Change directory permissions:</h2>
    <p align="center">
The company does not want anybody to have access to the drafts directory besides the user, researcher2. Based on this I removed execute permission from the group, as the picture indicates.  <br/>
<img src="https://i.imgur.com/39sf3Zm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
      <h2>Summary</h2>
      I assessed and modified all permissions to match the desired level of the organisation’s authorization policy. I used the commands:
cd = to enter the desired directory,
ls -la = to list the files,
Chmod = to change permissions.  <br/>

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
