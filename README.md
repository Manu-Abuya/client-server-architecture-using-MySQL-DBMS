# CLIENT-SERVER-ARCHITECTURE-USING-MySQL-DBMS.

TASK – Implement a Client Server Architecture using MySQL Database Management System (DBMS).
To demonstrate a basic client-server using MySQL Relational Database Management System (RDBMS), this is what I did:

1. Created and configured two Linux-based virtual servers (EC2 instances in AWS).


2. Install MySQL Server software in mysql server EC2 instance
    ```shell
    sudo apt update
    sudo apt install mysql-server
    
3. Install MySQL Client software in mysql client EC2 instance
    ```shell
    sudo apt update
    sudo apt install mysql-client
    
4. Enable communication between the MySQL server and client on EC2 instances:
    
    a. Both servers are on the same local virtual network and can use local IP addresses to communicate.

    b. Open TCP port 3306 on the MySQL server's Security Group:
    
        - In the 'mysql server' Security Group, add a new inbound rule.
        - Allow access only from the specific local IP address of the 'mysql client'.
        - This allows the MySQL client to connect to the server on port 3306.

5. Configure MySQL server to allow connection from remote hosts.
    ```shell
    sudo vi /etc/mysql/mysql.conf.d/mysqld.cnf
    ```
    
    In the bind-address and change the value from 127.0.0.1 to 0.0.0.0.
