# git push
Коротко: отправляет локальную ветку на [удаленный репозиторий](./remote_add_origin.md). 

Подробно: все локальные наработки, которые были [проиндексированы](./add.md) и [закоммичены](./commit.md) будут отправлены на удаленный репозиторий. 

### Использование
Общий вид:

`git push <имя_ветки_на_удаленном_репозитории> <имя_ветки_в_локальном_репозитории>`

Но есть нюанс: если планируется в дальнейшем копировать все изменения с локальной ветки *b_local* в ветку *b_remote* удаленного репозитория, можно единожды вызвать команду

`git push -u <b_remote> <b_local>`

После этого можно дальше просто выполнять

`git push`
___
[Назад](./readme.md)