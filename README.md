# stahovani_sracek
1. sudo apt update
2. sudo apt install apache2
3. sudo apt install dialog
4. sudo apt install phpmyadmin
5. v dialogu no, apache2
6. sudo apt search apache2 | grep php
7. sudo apt install libapache2-mod-php
8. sudo apt install mariadb-server nebo mysql-server
9. sudo su -
10. mysql
   - CREATE USER 'student'@'localhost' IDENTIFIED BY 'student';
   - GRANT ALL PRIVILEGES ON "*"."*" TO 'student'@'localhost' WITH GRANT OPTION;
   - flush privileges;
   - quit
11. cd /var/www/html
12. rm *
13. wget "link"
14. unlist "neco.zip"
15. mv wordpress/* ./
16. ps axu | grep apache //zjisteni na jakem uzivateli bezi
17. cd ..
18. chown www-data.www-data -R ./*
# zmena portu na kterem bezi
1. sudo apt install net-tools
2. netstat -vapnl | grep apache
3. cd /etc/apache2
4. grep port -r ./* //najdu soubor LIKE ports
5. mcedit ports.conf
   -upravit u Listen port
6. systemctl restart apache2
   # zaloha
1. mysqldump -u student -pstudent wordpress > /tmp/zaloha.sql //zaloha
2. cat /tmp/zaloha.sql | mysql -u student -pstudent wordpress //obnoveni
3. tar cvfz /tmp/zaloha.tar.gz /var/www/html/ //zaloha databaze
4. tar xvfz /tmp/zaloha.tar.gz -C /tmp //obnova databaze



   
