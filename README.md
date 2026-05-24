# HV_LinuxAssignment
LinuxAssignment - Assignment 
# Question 1:
Create the directory /home/ec2-user/webapp/ with three subdirectories inside it: scripts/, logs/, and config/ using a single mkdir -p command.
<img width="940" height="219" alt="image" src="https://github.com/user-attachments/assets/84ff55f9-758a-4042-96e1-21888e5a424b" />

Use cat > to create config/app.conf with two lines of content: APP_NAME=WebApp and PORT=8080. Save using Ctrl+D.
<img width="940" height="268" alt="image" src="https://github.com/user-attachments/assets/cd0c2337-3e7c-4ab3-a7bb-89bd78e183c4" />

Use touch to create an empty file at logs/app.log. Confirm it is 0 bytes using ls -l. 
<img width="940" height="197" alt="image" src="https://github.com/user-attachments/assets/59790087-4a5b-4b24-8eaa-303656aacf38" />

Set permissions: chmod 755 scripts/ and chmod 644 config/app.conf. Explain in your own words what 755 and 644 mean for owner, group, and others. 
<img width="940" height="164" alt="image" src="https://github.com/user-attachments/assets/2d962dd4-0929-44f4-9f0c-e8c1b5e06977" />

chmod 755 scripts/
rwxr-xr-x          i.e          (rwx…..r-x…..r-x)
Permission       rwx ->  Read, Write, Execute.
Group 		       r-x -> Read and Execute 
Others		       r-x -> Read and Execute

<img width="940" height="135" alt="image" src="https://github.com/user-attachments/assets/b18acce1-83f1-4c23-b6c6-3d441b9fd450" />

chmod 644 config/app.conf
rw-r--r--  e          (rw-…..r--…..r--)
Permission
Owner                       rw- ->  Read, Write.
Group 		       r-- -> Read only 
Others		       r-- -> Read only

Recursively change ownership of the entire webapp/ directory to root:root using chown -R. Then run ls -lR /home/ec2-user/webapp/ and share the output to confirm every file and folder shows root root as owner.
<img width="940" height="342" alt="image" src="https://github.com/user-attachments/assets/b6dd39a0-2539-4b63-ab93-0ca0bd19089e" />

# Question 2:

<img width="1503" height="780" alt="image" src="https://github.com/user-attachments/assets/2bf6cbe4-1f5b-4910-8ceb-5cdbacb2c3b1" />

<img width="1501" height="780" alt="image" src="https://github.com/user-attachments/assets/2df9b0d8-7f42-4fd3-ac0d-9b48d3eec40c" />

**Now given execute permission and run the scripts three times.**

<img width="1527" height="888" alt="image" src="https://github.com/user-attachments/assets/242eefc5-6460-4b7d-8b5b-0f0169f6ad78" />

**Verified log entry**
<img width="1495" height="343" alt="image" src="https://github.com/user-attachments/assets/85b59e9b-bcb9-4a06-a0a9-5c0de4fa1b8c" />

# Question 3:

**Created a group called writers**

<img width="1535" height="461" alt="image" src="https://github.com/user-attachments/assets/843b15b7-263a-4cdc-bca9-43446c3f91c3" />

**Created four users**
<img width="1498" height="638" alt="image" src="https://github.com/user-attachments/assets/2ae49b76-773a-471b-89ec-3ef2e08bb3a2" />

**Added write users to writers group**
<img width="1526" height="798" alt="image" src="https://github.com/user-attachments/assets/f6bcb7d2-1fba-4042-b02f-18a2fc26f261" />

**Change the group ownership of log_user.sh to writers: sudo chown root:writers /home/ec2-user/webapp/scripts/log_user.sh
Set permissions to 664 so writers group gets rw and others get r only: sudo chmod 664 /home/ec2-user/webapp/scripts/log_user.sh
Verify the permission output shows: -rw-rw-r--  root  writers  log_user.sh**

<img width="1507" height="417" alt="image" src="https://github.com/user-attachments/assets/b820c9d8-1531-406b-8556-15787582c619" />

**Switch to each user and test access to confirm it is working correctly:
Permission Layout (chmod 664):
chmod 664 log_user.sh
 6          6          4
Owner(rw)  Group(rw)  Others(r)
 root      writers    devuser3, devuser4**


 <img width="1497" height="758" alt="image" src="https://github.com/user-attachments/assets/62c2c5c9-797b-42db-8a97-771d354a684b" />

 <img width="1505" height="893" alt="image" src="https://github.com/user-attachments/assets/a4bc669f-f6b4-477c-96cf-fd72c2a43dfb" />

 <img width="1502" height="892" alt="image" src="https://github.com/user-attachments/assets/f73f1225-0b24-40f3-9798-b6cf109f13b6" />

 <img width="1507" height="943" alt="image" src="https://github.com/user-attachments/assets/c704868c-12ae-44c0-9582-9efb78985339" />










 


