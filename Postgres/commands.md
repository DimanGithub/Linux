# проверить версию postgresql
psql --version

# проверить запущен ли postgresql
systemctl status postgesql

# открыть файл для настройки 
sudo nano /etc/postgresql/13/main/postgresql.conf

# перезапуск службы POStgresql
systemctl restart postgresql

# получить доступ к psqlтерминалу как пользователь «postgres»
sudo -u postgres psql
или
su - postgres
psql
## после того как вошли можем задать пароль Для пользователя postqres
postgres=# \password postgres
## Создание нового пользователя с паролем
postgres=# Create user info_comp with password '123456';
#  список баз данных
 \l
