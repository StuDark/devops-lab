# Если имя ssh-key отличается от стандартного
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/<name>

# Альтернативный вариант (более правильный)
nano ~/.ssh/config
	Host github.com
		HostName github.com
		User git
		IdentityFile ~/.ssh/<name>
		AddKeysToAgent yes
