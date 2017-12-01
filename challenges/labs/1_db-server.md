* A command and output that shows the hostname of your database server
mysql> SELECT @@hostname hostname;
+----------+
| hostname |
+----------+
| nodo1    |
+----------+
1 row in set (0.01 sec)
* A command and output that reports the database server version
mysql> SHOW VARIABLES LIKE "%version%";
+-------------------------+------------------------------+
| Variable_name           | Value                        |
+-------------------------+------------------------------+
| innodb_version          | 5.7.20                       |
| protocol_version        | 10                           |
| slave_type_conversions  |                              |
| tls_version             | TLSv1,TLSv1.1                |
| version                 | 5.7.20                       |
| version_comment         | MySQL Community Server (GPL) |
| version_compile_machine | x86_64                       |
| version_compile_os      | Linux                        |
+-------------------------+------------------------------+
8 rows in set (0.01 sec)
* A command and output that lists all the databases in the server
mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| amon               |
| hive               |
| hue                |
| mysql              |
| oozie              |
| performance_schema |
| rman               |
| scm                |
| sentry             |
| sys                |
+--------------------+
11 rows in set (0.00 sec)
