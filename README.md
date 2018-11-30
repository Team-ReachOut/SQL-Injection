# SQL Injection

## Steps to Run

1. Create a database as `VMA` and create a table `users` in it with following fields :
- first_name
- last_name
- username
- password

2. Set username and password as `' ' OR '1' = '1'`. After this, login will be granted of some random user without username and password.

3. If we enter some particular username and password as `' ' OR '1' = '1'`, login will be granted of that particular user without password.

4. To delete the entire table, use the query :- `' UNION DROP TABLE USERS --;`.

5. For prevention of this, we can use the function :- `mysql_real_escape_string()`
