## Documentation of Lordchancellor's Project 5
- Summary of the Documentation
The project was all about implementing a client server architecture using the Mysql Data Management System.Two instances were launched on the AWS cloud named mysql server and my mysql client respectively. checcck the image below:
![The two servers](./images/the%two%servers) 
The aim was for the two virtual servers to be able to communicate through the respective terminal with one another using the local IP addresses. This was eventually achieved at the end of the implementation.
- The first command was `sudo apt update` followed by the installation of the mysql server wwhich was the major tool for the implementation of the project. The mysql server was installed with `sudo apt install mysql-server -y` on the mysql ubuntu virtual machine accesssed through the windows terminal. the hostname for the two virtual machines were change in other to easily differentiate them. For the mysql-client server, i ran `sudo hostnamectl set-hostname mysql-client` The image below was the outtput: ![hostname for client](./images/hostname)
 `sudo apt install mysql-client -y` was the command ran on the client's terminal after `sudo apt update` 
- On the ubuntu server terminal, i was able to set up mysql after a successful login, created a user, granted permission, and created a database. Check the image below for clear description:
![mysql setup](./images/mysql%setup)
- In other to allow connection from remote hosts, i ran `sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf` edited as instructed in the documentation, edited the inbound rules of the mysql server to MYSQL/Aurora, port 3306(By default) while the source of connection was the private IP of the mysql-client instance. the two servers were eventually able to communicate the same output on separate terminals and the images below were the output for the respective servers.
![database for mysql-server](./images/show%databases)
![database for mysql-client](./images/database%for%client)
- Thank you!