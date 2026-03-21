# Запуск отдельного namespace
sudo unshare --fork --pid --mount-proc bash
# Проверка
echo $$

