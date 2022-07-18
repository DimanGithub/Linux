# установка OpenSSH сервера
#sudo apt install openssh-server -y
# включение автозапуска
#sudo systemctl enable ssh
# проверка работоспособности утилиты
#ssh localhost
# изменение конфигурации
## сначало копируем конфигурацию
# sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_config.factory-defaults
## Затем открываем конфигурацию
#sudo vi /etc/ssh/sshd_config
###  PermitRootLogin -отключить возможность входа через root и пароль
###  PubkeyAuthentication - включить возможность входа через ключи
##  перезагрузить демон SSH. Соединение при этом будет разорвано и подключиться можно будет через новый порт и пользовательскую учетную запись (она должны быть предварительно создана).
#sudo systemctl restart ssh
# еще вариант подключения  port - 5555,  login - ansible, IpAddress 95.213.154.235 
ssh -p 55555 ansible@95.213.154.235   
# сгенерировать пару ключей.Команду нужно выполнять на своей рабочей станции от имени пользователя, который будет в дальнейшем подключаться к удаленному компьютеру.
#ssh-keygen -t rsa
# копирование ключа на удаленный сервер
#ssh-copy-id -i ~/.ssh/id_rsa.pub antoniusfirst@95.213.154.235
#ssh antoniusfirst@95.213.154.235
