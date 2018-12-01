# SQL Injection

## Steps to Run

1. Create a database as `VMA` and create a table `users` in it with following fields :
- first_name
- last_name
- username
- password

2. Visit localhost/security/sinin1.html. Set username and password as `' ' OR '1' = '1'`. After this, login will be granted of some random user without username and password.

3. If we enter some particular username and password as `' ' OR '1' = '1'`, login will be granted of that particular user without password.

4. To delete the entire table, use the query :- `' UNION DROP TABLE USERS --;`.

5. For prevention of this, we can use the function :- `mysql_real_escape_string()`. Adding these 2 lines will remove the special characters from input.
<br>
`$Fname = mysqli_real_escape_string($conn, $Fname);`
<br>
`$Password = mysqli_real_escape_string($conn, $Password);`

## Screenshots

<img src = "https://user-images.githubusercontent.com/14792027/49327733-ea4ce500-f58a-11e8-875c-00b7156bf698.png">   
<br>
<img src = "https://user-images.githubusercontent.com/14792027/49327734-ecaf3f00-f58a-11e8-952b-19810c9ac47c.png">   
<br>
<img src = "https://user-images.githubusercontent.com/14792027/49327738-ef119900-f58a-11e8-84c2-c012eb4ab020.png">   
<br>
<img src = "https://user-images.githubusercontent.com/14792027/49327739-f0db5c80-f58a-11e8-9c02-cb0517158296.png">   
<br>

