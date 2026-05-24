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

<img width="1527" height="888" alt="image" src="https://github.com/user-attachments/assets/242eefc5-6460-4b7d-8b5b-0f0169f6ad78" />



 


