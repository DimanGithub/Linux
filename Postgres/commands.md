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
#  список баз данных
 \l
