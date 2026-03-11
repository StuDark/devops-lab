# Проверка firewall
sudo ufw """should be installed"""  status
sudo ufw allow OpenSSH
sudo ufw enable
sudo ufw status verbose
