<h1>Modifying file permissions in Linux</h1>

<h2>Description</h2>
A research team at a fictional organization needs to update the file permissions for certain files and directories within the projects directory. By checking and updating these permissions will help keep their system secure. To complete this task, I performed the following tasks.
<br />

<h2>Walkthrough:</h2>

<h3 align="left">Check files and directory details</h3>
<img src="https://i.imgur.com/kHr9Urh.png" height="100%" width="100%" alt="Check files and directory"/>
 <p>
  The command, ls -la, to display all files and directories including hidden files and the permissions for each file (including hidden ones) and directory. 
 </p>
<br />
<br />

<h3 align="left">The permission strings</h3>
<p>
In the screenshot above, each line shows either a file and directory and the permissions. In the first block of text for each line are 10 characters that represent the permissions authorized for a user, group, and others. 

Permissions in a file system are r (read), w (write), and x (execute).

The 1st character is either a d, for directory or (hyphen) -, for file.

The 2nd-4th characters are the permissions for the user. If a hyphen is present instead of either r, w, or x, then the permission is not granted. 

The 5th-7th characters are the permissions for the group. If a hyphen is present instead of either r, w, or x, then the permission is not granted. 

The 8th-10th characters are the permissions for others. Others consist of users that are neither the user nor the group. If a hyphen is present instead of either r, w, or x, then the permission is not granted. 

For example, the file permissions for the file project_k.txt are -rw-rw-rw-. The first character, -, indicates that this is a file. The next 3 characters indicate that the user can read and write on this file, but not execute. These are the same permissions for the group and others. No one has permission to execute the file. 
</p>
<br />
<br />

<h3 align="left">Change file permissions</h3>
<img src="https://i.imgur.com/QiHSdXm.png" height="100%" width="100%" alt="Change file permissions"/>
 <p>
  The organization has stated that others shouldn’t be able to write on the project_k.txt file. From the screenshot from above, the write permission is granted for other in the project_k.txt file.

  Using the chmod command, I can add, remove, or assign permissions to either the user, group, or others.

  The chmod command is followed by either u (user), g (group), or o (other), then followed by + (add permission) or hyphen (- for remove permission), and finally r, w, or x. 

  In the screenshot above, the write permission is removed from others in the project_k.txt file. After this, the ls -l is command is used to check if the write permission is removed.
 </p>
<br />
<br />

<h3 align="left">Change file permissions on a hidden file</h3>
<img src="https://i.imgur.com/BwDUsZk.png" height="100%" width="100%" alt="Change file permissions on a hidden file"/>
 <p>
  The research team archived the file project_x.txt and does not want anyone to be able to write on this file, however, the user should still be able to read this file. 

  Hidden files are indicated with a . in front of the file name. In the screenshot below, project_x.txt is a hidden file.
  
  The write permission is removed from both the user and group for the hidden file, project_x.txt.
  
  I used ls -l to check if the write permission is removed. 
 </p>
<br />
<br />

<h3 align="left">Change directory permissions</h3>
<img src="https://i.imgur.com/dDCYvwi.png" height="100%" width="100%" alt="Change directory permissions"/>
 <p>
  The organization wants user, researcher2, to have access to the drafts directory and its contents. This means no one else should have access to this directory. From the first screenshot above, the group has the execute permission. 
  
  Permissions to the directory can also be modified for different users.

  In the screenshot above, I removed the execute permission from the group for the directory, drafts/ . 

  I used the command ls -la to not only display all the files, directories, and hidden files and all permissions to confirm the change was successful.

 </p>
<br />
<br />

<h2>Summary</h2>
I updated permissions for certain files and directories to ensure that only authorized users can access and act on them. I learned how to view all files and directories (including hidden files) and their permissions with the ls -la command and to update permissions with the chmod command. 
<br />
