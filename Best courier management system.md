### Best courier management system has SQL injection vulnerabilities

##### Source code download：https://www.sourcecodester.com/php/16848/best-courier-management-system-project-php.html

##### Version：V1.0（2023/9/21/12:14）

Vulnerability Description: The system has an SQL injection vulnerability, which allows attackers to obtain database information and gain website control permissions by inserting malicious SQL statements.

**1、sql injection vulnerability was found on the page [print_pdets.php] through code audit**

![image-20240122164434283](https://github.com/modian-un/CVE/blob/main/Best%20courier%20management%20system.assets/image-20240122164434283.png)

Vulnerability verification:

**2、Log in to the system first **

![image-20240122164821985](https://github.com/modian-un/CVE/blob/main/Best%20courier%20management%20system.assets/image-20240122164821985.png)

**3、The ids parameter of the 【/print_pdets.php】 page was not filtered, resulting in sql injection. full the url :"http://192.168.137.130/print_pdets.php?ids=1"**

![image-20240122165001075](https://github.com/modian-un/CVE/blob/main/Best%20courier%20management%20system.assets/image-20240122165001075.png)

**4、The database name was successfully popped using sqlmap verification**

![image-20240122165258751](https://github.com/modian-un/CVE/blob/main/Best%20courier%20management%20system.assets/image-20240122165258751.png)

![image-20240122165354125](https://github.com/modian-un/CVE/blob/main/Best%20courier%20management%20system.assets/image-20240122165354125.png)
