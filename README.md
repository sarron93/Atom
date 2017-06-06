# Atom
Установка:
1. Вирутальный хост
```
<VirtualHost *:80>
	ServerName atom.loc
	DocumentRoot "C:/xampp/htdocs/Atom"
	<Directory "C:/xampp/htdocs/Atom">
		AllowOverride All
		Order Allow,Deny
        	Allow from All
		<IfModule mod_rewrite.c>
			RewriteEngine On
			RewriteBase /
			RewriteRule ^index\.php$ - [L]
			RewriteCond %{REQUEST_FILENAME} !-f
			RewriteCond %{REQUEST_FILENAME} !-d
			RewriteRule . /index.php [L]
		</IfModule>		
	</Directory>
</VirtualHost>
```
2. Переименовываем файл wp-config-sample.php в wp-config.php
3. Следовать инструкции тут https://www.digitalocean.com/community/tutorials/wordpress-lamp-ubuntu-16-04-ru
с раздела Настройка файла конфигурации WordPress.

# Админу 
На свое усмотрение, но для инфы вот ресурс https://www.digitalocean.com/community/tutorials/wordpress-lamp-ubuntu-16-04-ru
