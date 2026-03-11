# Проверка процессов

ps aux
top
htop (should be installed)

# namespace - изоляция процессов

sudo unshare  --fork --pid --mount-proc bash

