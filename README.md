# solutions
Solutions for developers

17

Please follow these steps to reset your MySQL Password on Windows:

Before you attemptto execute the below steps make sure you first terminate the MySQL Service @ services.msc(You can type service on the bottom left bar and click services)

Step 1: Create a .txt file in you C: drive and paste this ALTER USER 'root'@'localhost' IDENTIFIED BY 'YourNewPassword'; 
You may replace your 'YourNewPassword' from above line withh your new root password.
Save the file under C:\\reset.txt.

Step 2: Run CMD.exe as Admin (Start->Cmd->Right Click->Run as Administrator)

Step 3: Type in cmd: cd "C:\Program Files\MySQL\MySQL Server 8.0\bin"

Step 4: Create “Data” Folder under "C:\Program Files\MySQL\MySQL Server 8.0\ (if already exists delete its contents!)

Step 5: Type in cmd: mysqld --initialize

Step 6: Type in cmd: mysqld --init-file=C:\\reset.txt

Login with root user account and the password set above on mysql.

Lastly Delete C:\ change_mysql_pwd.txt file
