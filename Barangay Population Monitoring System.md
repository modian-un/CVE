### Barangay Population Monitoring System has SQL injection vulnerabilities

##### Source code download：https://www.sourcecodester.com/php/17109/barangay-population-monitoring-system-using-php-mysql-and-chartjs-source-code.html

##### Version：2024/1/15/15:06

Vulnerability Description: The system has an SQL injection vulnerability, which allows attackers to obtain database information and gain website control permissions by inserting malicious SQL statements.

**1、Log in to the system first (default password: admin/admin)**

![image-20240120132623791](https://github.com/modian-un/CVE/blob/main/Barangay%20Population%20Monitoring%20System.assets/image-20240120132623791.png)

**2、Click Masterlist and click Delete button to grab the packet**

![image-20240120132717476](https://github.com/modian-un/CVE/blob/main/Barangay%20Population%20Monitoring%20System.assets/image-20240120132717476.png)

**3、The resident parameter of the 【/endpoint/delete-resident.php】 page was not filtered, resulting in sql injection. full the url :"http://192.168.137.130/endpoint/delete-resident.php?resident=2"**

![image-20240120132958612](https://github.com/modian-un/CVE/blob/main/Barangay%20Population%20Monitoring%20System.assets/image-20240120132958612.png)

**4、The database name was successfully popped using sqlmap verification**

![image-20240120133212599](https://github.com/modian-un/CVE/blob/main/Barangay%20Population%20Monitoring%20System.assets/image-20240120133212599.png)

![image-20240120133307683](https://github.com/modian-un/CVE/blob/main/Barangay%20Population%20Monitoring%20System.assets/image-20240120133307683.png)
