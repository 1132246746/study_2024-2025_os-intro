#Лабораторная работа №2

##Выполнил Шилов Александр Ильич

##Установка программного обеспечения

###Установка git
####Установим git:
```bash
dnf install git
```

###Установка gh
####Установим gh:
```bash
dnf install gh
```

##Базовая настройка git
####Зададим имя и email владельца репозитория:
```bash
git config --global user.name "1132246746"
git config --global user.email "sashandr000chanel000999000@gmail.com"
```

####Настроим utf-8 в выводе сообщений git:
```bash
git config --global core.quotepath false
```

####Зададим имя начальной ветки (будем называть её master):
```bash
git config --global init.defaultBranch master
```

####Параметр autocrlf:
```bash
git config --global core.autocrlf input
```

####Параметр safecrlf:
```bash
git config --global core.safecrlf warn
```

##Создание ключей ssh

####по алгоритму rsa с ключём размером 4096 бит:
```bash
ssh-keygen -t rsa -b 4096
```

##Создание ключей pgp

##Генерируем ключ
```bash
gpg --full-generate-key
```

##Добавление PGP ключа в GitHub

####Выводим список ключей и копируем отпечаток приватного ключа:
```bash
gpg --list-secret-keys --keyid-format LONG
```

##Настройка автоматических подписей коммитов git

####Используя введёный email, указываем Git применять его при подписи коммитов:
```bash
git config --global user.signingkey <PGP Fingerprint>
git config --global commit.gpgsign true
git config --global gpg.program $(which gpg2)
```

##Вывод
####Я изучил идеологию и применение средств контроля версий.
####Я освоил умения по работе с git.
