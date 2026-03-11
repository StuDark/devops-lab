# Создание пользователя sudo

adduser user
usermod -aG sudo user

# Добавление SSH-ключа пользователю sudo

mkdir -p /home/user/.ssh
chmod 700 /home/user/.ssh
cp /root/.ssh/autorized_keys /home/user/.ssh/
chmod 600 /home/user/.ssh/autorized_keys
chown -R user:user /home/user/.ssh
# проверить вход под новым пользователем в отдельном окне терминала
whoami
groups user
# Отключение root

nano /etc/ssh/sshd_config
PermitRootLogin yes --> no
PasswordAuthentication yes --> no
systemctl restart ssh
