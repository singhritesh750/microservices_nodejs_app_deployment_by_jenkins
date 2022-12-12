# Readme

## Please run the following command to create the database and table on mysql server before run the app.js
* CREATE DATABASE employees_db
* USE employees_db
* CREATE TABLE IF NOT EXISTS `EMPLOYEES` (
   emp_id int(11) NOT NULL PRIMARY KEY AUTO_INCREMENT,
   emp_name varchar(255) NOT NULL,
   emp_contact varchar(10),
   emp_add varchar(255) DEFAULT false
   ) ENGINE=InnoDB DEFAULT CHARSET=utf8;

## Change the connection url in the code with the mysql servers url (check conn.js)


# Error lists:

Error: connect ECONNREFUSED 3.87.135.15:3306 :
https://in.search.yahoo.com/search?fr=mcafee&type=E210IN91213G91674&p=Error%3A+connect+ECONNREFUSED+3.87.135.15%3A3306
https://stackoverflow.com/questions/42899916/getting-error-connect-econnrefused-127-0-0-13306-while-connecting-to-mysql
https://www.apachefriends.org/index.html
https://www.wikihow.com/Install-XAMPP-on-Linux

at TCPConnectWrap.afterConnect [as oncomplete] (net.js:1138:16) :
https://in.search.yahoo.com/search?fr=mcafee&type=E210IN91213G91674&p=at+TCPConnectWrap.afterConnect+%5Bas+oncomplete%5D+(net.js%3A1138%3A16)
https://stackoverflow.com/questions/64281957/error-connect-econnrefused-185-248-177-1103306-at-tcpconnectwrap-afterconnect

ERROR 2002 (HY000): Can't connect to local server through socket '/run/mysqld/mysqld.sock'
https://in.search.yahoo.com/search?fr=mcafee&type=E210IN91213G91674&p=ERROR+2002+(HY000)%3A+Can%27t+connect+to+local+server+through+socket+%27%2Frun%2Fmysqld%2Fmysqld.sock%27
https://stackoverflow.com/questions/11657829/error-2002-hy000-cant-connect-to-local-mysql-server-through-socket-var-run
https://sebhastian.com/mysql-error-2002/#:~:text=To%20conclude%2C%20the%20ERROR%202002%20happens%20when%20your,are%20different%20ways%20to%20start%20your%20MySQL%20server.

Error: Host 'ec2.amazonaws.com' is not allowed to connect to this MySQL server
https://in.search.yahoo.com/search;_ylt=AwrPofj9Spdje.gbdUm7HAx.;_ylc=X1MDMjExNDcyMzAwMwRfcgMyBGZyA21jYWZlZQRmcjIDc2ItdG9wBGdwcmlkA2lGVTRtaUowUjk2U2pEZWd4NXhXYUEEbl9yc2x0AzAEbl9zdWdnAzAEb3JpZ2luA2luLnNlYXJjaC55YWhvby5jb20EcG9zAzAEcHFzdHIDBHBxc3RybAMwBHFzdHJsAzc4BHF1ZXJ5A0Vycm9yJTNBJTIwSG9zdCUyMCdlYzIuYW1hem9uYXdzLmNvbSclMjBpcyUyMG5vdCUyMGFsbG93ZWQlMjB0byUyMGNvbm5lY3QlMjB0byUyMHRoaXMlMjBNeVNRTCUyMHNlcnZlcgR0X3N0bXADMTY3MDg1OTUzNA--?p=Error%3A+Host+%27ec2.amazonaws.com%27+is+not+allowed+to+connect+to+this+MySQL+server&fr2=sb-top&fr=mcafee&vm=r&type=E210IN91213G91674
https://www.linuxandubuntu.com/home/sqlstatehy000-1130-host-not-allowed-to-connect-to-this-mysql-server
correct syntax for our use-case is 
`CREATE USER 'root'@'54.91.161.193' IDENTIFIED BY '';`
`GRANT ALL ON `employees_db`.* to 'root'@'54.91.161.193';`
`FLUSH PRIVILEGES;`
https://cloudaffaire.com/aws/1130-host-amazon-ec2-ip-is-not-allowed-to-connect-to-this-mysql-server/

code: 'ER_HOST_NOT_PRIVILEGED', errno: 1130
https://in.search.yahoo.com/search;_ylt=AwrKC.zETpdj1QEcrxK7HAx.;_ylc=X1MDMjExNDcyMzAwMwRfcgMyBGZyA21jYWZlZQRmcjIDc2ItdG9wBGdwcmlkAy5WT2lnQ1o1U3llZklVS1MzOC5lNEEEbl9yc2x0AzAEbl9zdWdnAzAEb3JpZ2luA2luLnNlYXJjaC55YWhvby5jb20EcG9zAzAEcHFzdHIDBHBxc3RybAMwBHFzdHJsAzQzBHF1ZXJ5A2NvZGUlM0ElMjAnRVJfSE9TVF9OT1RfUFJJVklMRUdFRCclMkMlMjBlcnJubyUzQSUyMDExMzAEdF9zdG1wAzE2NzA4NjA0OTM-?p=code%3A+%27ER_HOST_NOT_PRIVILEGED%27%2C+errno%3A+1130&fr2=sb-top&fr=mcafee&vm=r&type=E210IN91213G91674
https://www.tecmint.com/fix-error-1130-hy000-host-not-allowed-to-connect-mysql/
correct syntax for our use-case is 
`mysql> SELECT host FROM mysql.user WHERE user = "root";`
`CREATE USER 'root'@'54.91.161.193' IDENTIFIED BY '';`
`GRANT ALL ON `employees_db`.* to 'root'@'54.91.161.193';`
`FLUSH PRIVILEGES;`

ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'IDENTIFIED BY "" ' at line 1
https://in.search.yahoo.com/search?fr=mcafee&type=E210IN91213G91674&p=ERROR+1064+(42000)%3A+You+have+an+error+in+your+SQL+syntax%3B+check+the+manual+that+corresponds+to+your+MySQL+server+version+for+the+right+syntax+to+use+near+%27IDENTIFIED+BY+%22%22%27+at+line+1
https://www.tutorialspoint.com/resolve-mysql-error-1064-42000-you-have-an-error-in-your-syntax
https://stackoverflow.com/questions/52372165/mysql-error-1064-42000-you-have-an-error-in-your-sql-syntax
https://stackoverflow.com/questions/18742492/error-1064-42000-you-have-an-error-in-your-sql-syntax
