# Шпаргалка по git

#### Разделы
1. [Основные](#main) настройки
2. [Базовые](#base) команды
3. [Bетвления](#branch) 
4. Настройка [ssh](#ssh)
5. [Полезные ссылки](#links)

### Преподаватель
 Николай
 **Мищенков**
<hr/>

### <a id="main"></a> Основные настройки git

* #### git config --global user.name &lt;name&gt; <br/> `указать имя пользователя`
* #### git config --global user.email &lt;abc@main.com&gt; <br/> `указать его эл/почту`
* #### git config --global core.editor &lt;editor executable file URL&gt; <br/> `выбрать редактор для коммитов`
* #### git config --global init.defaultHead &lt;master branch new name&gt; <br/> `поменять имя master-ветки на другое (main например)`

<hr>

### <a id="base"></a> Команды

* #### git init <br/> `иницировать локальный git-репозиторий в текущей папке`
* #### git status <br/> `смотрим статус, что творится в репозитории`
* #### git add &lt;url&gt;<br/> `добавить в отслеживание (stage) все файлы из текущей директории`
* #### git commit [-a] [-m "commit message"] <br/> `создать коммит (-a только по tracked-файлам, можно писать сразу без git add)`
* #### git log <br/> `посмотреть подробный журнал коммитов (хэш-код автор дата сообщение из (... -m "commit message"... )) (любое фиксирующее действие в git'е представляет собой коммит!)`
* #### git log --oneline <br/> `--oneline выдает журнал в сокращенном виде с короткими хэшами, копипаст которых достаточен для git-команд, где требуется хэш коммита`
* #### git log [master] <br/> `при переводе указателя HEAD журнал будет видно только до HEAD, c master будут видны все коммиты после HEAD до последнего в текущей ветке master`
* #### git checkout &lt;commit hash&gt; <br/> `переход от одного коммита к другому (хеш можно сокращенный!)`
* #### git checkout master <br/> `вернуться к актуальному состоянию и продолжить работу, вернуть HEAD на master`
* #### git diff <br/> `увидеть разницу между текущим файлом и закоммиченным файлом`

<hr>

### <a id="branch"></a> Ветвления 
* #### git branch <br/> `посмотреть список веток (текущая*)`
* #### git checkout -b &lt;newbranch&gt; <br/> `создать ветку и перейти в нее`
* #### git branch -D &lt;branch&gt; <br/> `удалить ветку`

<hr>

### <a id="ssh"></a> SSH настройка
* #### ssh-keygen -t rsa -b 4096 -C &lt;credentials&gt; <br/> `сгенерировать пару ssh-ключей (открытый и закрытый)`
<code>Публичный ключ добавляется на Github (Settings -> SSH and GPG)</code>

* #### eval $(ssh-agent -s) <br/> `инициировать процесс ssh соединения`
* #### ssh-add &lt;url закрытого ключа&gt; <br/> `привязать к ssh соединению закрытый ключ, публичный должен быть сохранен на удаленном репозитории`
* #### ssh -T git@github.com <br/> `тест соединения с github'ом`

<hr>

### <a id="links"></a> Полезные ссылки

> [гит для новичков](https://habr.com/ru/post/541258/)

> [как оформлять .md файлы](https://gist.github.com/Jekins/2bf2d0638163f1294637)

> [соглашение о коммитах](https://www.conventionalcommits.org/ru/v1.0.0-beta.2/)

> [коротко о ssh](https://habr.com/ru/sandbox/166705/)
