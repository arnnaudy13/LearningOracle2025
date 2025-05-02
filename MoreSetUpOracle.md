| More Set Up Oracle |

Adding schema browser user (kinda like admins not ADMIN. So yeah. I will revise this but this are the following link for the tutorial)

1. https://stackoverflow.com/questions/18403125/how-to-create-a-new-schema-new-user-in-oracle-database-11g

2. https://stackoverflow.com/questions/33330968/error-ora-65096-invalid-common-user-or-role-name-in-oracle-database

3. https://stackoverflow.com/questions/33591002/oracle-11g-user-exists-but-when-try-to-drop-it-says-user-doesnt-exist

| My Tutorial (Kinda) | 

1. in SQL Plus open it and use the first username and password you set up remember use 'as sysdba'. Make sure you are connected.

2. Then after that enter 'create user [name] identified by [password];'

3. If you get,
ERROR at line 1:
ORA-65096: invalid common user or role name

do the following, ' alter session set "_ORACLE_SCRIPT"=true; ' 

it's a bit risky but since we are still learning, we will use the only way to create user first. Then do point 2.

4. You can check all of the user by 'select username from dba_users;'

5. Giving access to the user 'grant create session to [name];' this will let you connect to the database as the user.

6. More access. 
SQL> grant create session to [name];
SQL> grant create table to [name];
SQL> grant unlimited tablespace to [name];

you can check the user privilage by log in a new window SQL Plus as your new user. 
Then enter, 'select * from session_privs;' 

also if granting access have problemn use this 'alter session set "_ORACLE_SCRIPT"=true;' 

7. To add table to user by entering this in SQL Plus,
   
SQL> create table name.tablename(a number);

You can alter the table in Navicat. This only create a new table for that user to modified/used.

8. Then after everything remember to 'alter session set "_ORACLE_SCRIPT"=false;' 


