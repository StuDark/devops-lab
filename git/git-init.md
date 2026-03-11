# Инициализация Git и новой репы с устройства

# Создать ssh-key на устройстве, обозвать ассоциативно с устройством
ssh-keygen -t ed25519 -f ~/.ssh/<name>
cat ~/.ssh/<name>.pub
# Добавить key в лк ресурса, используемого для Git

# Добавление автора коммитов
git config --global user.name "<Name>"
git config --global user.email "<email@mail.com>"
git config --global init.defaultBranch main
git config --list
cd devops-lab
pwd
git init
ls -a
nano .gitignore <-- *.log *.tmp
git add .
git commit -m "initial <rep>"
# Создать репу на ресурсе, дать название

# Подключение
git remote add origin git@github.com:<username>/<rep>.git
git remote -v

# Подключение, только первый раз
git push -u origin main

# Далее только так
git add .
git commit -m "<описание изменений>"
git push

# С другого устройства
git pull

# Узнать, что было изменено
git status
