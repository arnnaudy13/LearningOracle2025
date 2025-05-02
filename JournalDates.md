[01/05/25]
I manage to set up the browser and understand the difference between Oracle and SQL Server. 
When you already understand the fundamental of SQL it's not as hard but there's still tricky process to understand the process. 
I still have like a lot of questions. Like can you make more than one database similiar like SQL? Can you make like an empty database? Because my process have to go through a template database. 
But we will se tomorrow. See yaaaaaa!

[02/05/25]
Learn a lot by learning from this https://github.com/Thanaraklee/Exploring-and-Analyzing-Data-in-Oracle-Database.git

But of course there will be some obstacle and here there go. I will fix it tonight. 
SQL> create user testing identified by 12345;
create user testing identified by 12345       *
ERROR at line 1:
ORA-65096: invalid common user or role name


SQL> create user ayliefia identified by adminuser;
create user ayliefia identified by adminuser            *
ERROR at line 1:
ORA-65096: invalid common user or role name

SQL> alter session set "_ORACLE_SCRIPT"=true;
Session altered.

SQL> create user ayliefia identified by adminuser;
User created.

SQL> alter session set "_ORACLE_SCRIPT"=false;
Session altered.

SQL> alter session set "_ORACLE_SCRIPT"=true;
Session altered.

SQL> alter session set "_ORACLE_SCRIPT"=false;
Session altered.

SQL> grant create sequence to naudy_db;
Grant succeeded.

