## MySql Cheatsheet
Bash login:
```bash
mysql -h {hostname} -u username -p {databasename}
```

Commands:
```mysql
SHOW DATABASES;
USE {Database name};
SHOW TABLES;
DESCRIBE {Table name};

SELECT field1, field2,...fieldN 
FROM table_name1, table_name2...
[WHERE Clause]
[OFFSET M ][LIMIT N];

```
Additional reference at:
https://www.tutorialspoint.com/mysql/index.htm
