# проверить версию postgresql
psql --version

# проверить запущен ли postgresql
systemctl status postgesql

# открыть файл для настройки 
sudo nano /etc/postgresql/12/main/postgresql.conf
sudo nano /etc/postgresql/12/main/pg_hba.conf

# перезапуск службы POStgresql
systemctl restart postgresql

# получить доступ к psqlтерминалу как пользователь «postgres»
sudo -u postgres psql
или
su - postgres
psql
## после того как вошли можем задать пароль Для пользователя postqres
postgres=# \password postgres
## Создание нового пользователя info_comp с паролем 123456
postgres=# Create user info_comp with password '123456';
## Создание базы данных
postgres=# Create database test_db;
## Дать права на управление базой данных пользователю info_comp
postgres=# grant all privileges on database test_bd to info_comp;
##  список баз данных
 \l
 ## выход в консоль
  \q
 # Подключение к базе данных от пользователя info_comp
 psql -h localhost test_db info_comp
 
 # перезапуск базы данных
 Root~# systemctl restart postgresql
 
 
