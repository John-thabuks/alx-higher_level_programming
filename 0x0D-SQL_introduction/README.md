# 0x0D. SQL - Introduction
`SQL` `MySQL`

# Concepts
*For this project, we expect you to look at these concepts:*

- [Databases](https://alx-intranet.hbtn.io/concepts/37)
- [Databases](https://alx-intranet.hbtn.io/concepts/556)


# Resources
### Read or watch:

- [What is Database & SQL?](https://alx-intranet.hbtn.io/rltoken/yyRKTEdRkYEVlRgZPbasjw)
- [A Basic MySQL Tutorial](https://alx-intranet.hbtn.io/rltoken/sV2PtK5YfQsXWW1malRZ5Q)
- [Basic SQL statements: DDL and DML *(no need to read the chapter “Privileges”)*](https://alx-intranet.hbtn.io/rltoken/IUKo4-UaRZSKPvXr5u9oBw)
- [Basic queries: SQL and RA](https://alx-intranet.hbtn.io/rltoken/rXKvu2u7vg1Hj6bnX7UgMg)
- [SQL technique: functions](https://alx-intranet.hbtn.io/rltoken/-Riv_dzSYsJyvy-LlaO6Mg)
-[SQL technique: subqueries](https://alx-intranet.hbtn.io/rltoken/QpIXoR--8eBIaidgSWYsBQ)
- [What makes the big difference between a backtick and an apostrophe?](https://alx-intranet.hbtn.io/rltoken/Gt0nFJPJRwW2Y0izzwbVrw)
- [MySQL Cheat Sheet](https://alx-intranet.hbtn.io/rltoken/wLQZvDtRCG9eQ69c8jvYVA)
- [MySQL 8.0 SQL Statement Syntax](https://alx-intranet.hbtn.io/rltoken/HmdmLiYBM0Q34iCYPWd9XQ)


# More Info
## Comments for your SQL file:
```sql
$ cat my_script.sql
-- 3 first students in the Batch ID=3
-- because Batch 3 is the best!
SELECT id, name FROM students WHERE batch_id = 3 ORDER BY created_at DESC LIMIT 3;
$
```

## Install MySQL 8.0 on Ubuntu 20.04 LTS
```sql
$ sudo apt update
$ sudo apt install mysql-server
...
$ mysql --version
mysql  Ver 8.0.25-0ubuntu0.20.04.1 for Linux on x86_64 ((Ubuntu))
$
```
Connect to your MySQL server:
```sql
$ sudo mysql
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 11
Server version: 8.0.25-0ubuntu0.20.04.1 (Ubuntu)

Copyright (c) 2000, 2021, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
mysql> quit
Bye
$
```
## Use “container-on-demand” to run MySQL
### In the container, credentials are `root/root`

- Ask for container `Ubuntu 20.04`
- Connect via SSH
- OR connect via the Web terminal
- In the container, you should start MySQL before playing with it:
```sql
$ service mysql start                                                   
 * Starting MySQL database server mysqld 
$
$ cat 0-list_databases.sql | mysql -uroot -p                               
Database                                                                                   
information_schema                                                                         
mysql                                                                                      
performance_schema                                                                         
sys                      
$
```
#### In the container, credentials are `root/root`