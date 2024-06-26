# git status
Позволяет проверить, на какой стадии или в каком состоянии находится проект.

### Использование 
`git status`
____
## Состояния
Файлы проекта либо находятся под версионным контролем (**отслеживаемые**), либо нет (**не отслеживаемые, untracked**). 

### 1. untracked
~~Ты кто такой, я тебя не знаю~~

Файлы, которые не были добавлены в репозиторий вообще, либо их нет в последнем сохраненном состоянии проекта(снимок, snapshot, коммит). 
> Примечание:
если вызвать команду `git status` вне каталога GIT-репозитория, консоль благополучно ругнется
>>fatal: not a git repository (or any of the parent directories): .git

### 2. Отслеживаемые
~~Я тебя запомнил~~

Как следует из текста выше, это файлы, которые уже успели добавить в репозиторий. Особенность этих файлов в том, что они могут находиться на 3х стадиях.
1. **modified** - что-то поправили в этих файлах, но дальше эти изменения не пошли.
Сообщение при вызове `git status`: 
> Changes not staged for commit: 
2. **staged** - мы решили, что хотим сохранить изменения из стадии 1. С помощью команды [add](./add.md) индексируем изменения (говорим GIT'у, что, возможно, захотим сделать из них снимок), но не сохраняем пока в репозитории. Сообщение при вызове `git status`: 
> Changes to be committed:  
3. **commited** - далее мы решили, что проиндексированные изменения хотим таки сохранить в репозитории. Используем команду [`git commit`](./commit.md), и вуаля: мы создали новый снимок(он же shapshot, он же коммит). 

> Примечание 1:
если после индексации изменений снова отредактировать какой-либо файл проекта, вызов git status покажет у него одновременно 2 состояния ("Changes to be committed" и "Changes not staged for commit"), и, если приступить к commit, то сохранятся только те изменения, что были проиндексированы. 

>Примечание 2:
Команда `git status` позволяет увидеть только состояние файлов. Чтобы узнать подробнее, какие именно изменения были внесены, что из них было подготовлено для сохранения ([add](./add.md), ага), используйте команду `git diff`
___
[Назад](./readme.md)