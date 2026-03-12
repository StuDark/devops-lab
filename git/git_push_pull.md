# Смотреть изменения
git status
# Подробнее
git diff
# Включить короткий формат
git config --global status.short true

# Отправка коммита/получение
# Все файлы
git add .
# Один файл
git add <path>/<name>.<format>
git commit -m "<commit_name>"
git push
git pull

# Отмена незакоммиченных изменений
# В одном файле
git restore <file_name>
# Все изменеия
git restore .
# Если в git add добавлено, но не закоммичено
git restore --staged .
git restore .
# Откат к последнему коммиту (опасно)
git reset --hard HEAD
# Если отправлено на GitHub
git revert HASH_<COMMIT>
