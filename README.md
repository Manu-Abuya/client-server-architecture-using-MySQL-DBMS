# CLIENT-SERVER-ARCHITECTURE-USING-MySQL-DBMS.

TASK – Implement a Client Server Architecture using MySQL Database Management System (DBMS).
To demonstrate a basic client-server using MySQL Relational Database Management System (RDBMS), this is what I did:

1. Created and configured two Linux-based virtual servers (EC2 instances in AWS).

![server and client ec2 instances](https://github.com/Manu-Abuya/client-server-architecture-using-MySQL-DBMS./blob/master/Screenshot%20from%202023-06-02%2015-14-47.png?raw=true)

2. Install MySQL Server software in mysql server EC2 instance
    ```shell
    sudo apt update
    sudo apt install mysql-server
    
3. Install MySQL Client software in mysql client EC2 instance
    ```shell
    sudo apt update
    sudo apt install mysql-client
