# stahovani_sracek
1. sudo apt update
2. sudo apt install apache2
3. sudo apt install dialog
4. v dialogu no, apache2
5. sudo apt search apache2 | grep php
6. sudo apt install libapache2-mod-php
7. sudo apt install mariadb-server nebo mysql-server
8. sudo su -
9. mysql
   - CREATE USER 'student'@'localhost' IDENTIFIED BY 'student';
   - GRANT ALL PRIVILEGES ON *.* TO 'student'@'localhost' WITH GRANT OPTION;
   - flush privileges;
   - quit
10. cd /var/www/html
11. rm *
12. wget "link"
13. unlist "neco.zip"
14. mv wordpress/* ./
15. ps axu | grep apache //zjisteni na jakem uzivateli bezi
16. cd ..
17. chown www-data.www-data -R ./*
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



   
