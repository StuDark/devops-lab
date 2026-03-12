# Проверка процессов

ps aux
top
htop (should be installed)

# Показать PID конкретного процесса
ps aux | grep <process>

# namespace - изоляция процессов

sudo unshare  --fork --pid --mount-proc bash

