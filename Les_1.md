# Инструкция по работе с Git
## Что такое Git
Git - это одна из самых популярных реализаций, распределенных систем контроля версий с локальными и удаленными репозиториями.
## Подготовка репозитория
Для создания репозитория используем команду *git init*. У вас создасться репозиторий (появится скрытая папка .git)
## Создание коммитов
### Git add
Для добавления изменений в коммит используется команда *git add <имя файла>*
### Git status
Для того чтобы посмотреть состояние репозитория используется команда *git status*
при использовании этой команды вы увидите были ли изменения в файлах или нет.
### Git commit
Для того чтобы создать коммит(сохранение) используется команда *git commit* Для этого сначала используем *git add <имя файла>* а после *git commit -m* где *-m*, команда для присвоения коммиту имени. Либо используем более короткую команду *git commit -am* где *-am*, команда для одновременного сохранения и присвоения коммиту имени.
### Git log
Для того чтобы посмотреть историю созданных коммитов используется команда *git log*. Для того чтобы покинуть просмотр истории на английской раскладке нажать клавишу *q*. Для более упрощенного просмотра истории коммитов используется команда *git log --oneline*.
### Git checkout 
Это команда для перемещения между коммитами(сохраненными версиями файлов) Для использования данной команды вводим сначала команду *git log* после выбираем необходимый нам коммит и в команду *git checkout* добавляем последние 4 знака необходимого лога(коммита) прим. *git checkout ea6f* Для возвращения на актуальную версию используем команду *git checkout master*.
## Прочие команды 
### Git help
Данная команда *git --help* покажет все возможные команды git.
### Git diff
Команда *git diff* показывает разницу между текущей версией и последней "закоммиченной" версией.
### Git version
Команда *git --version* покажет вам какая версия git у вас установлена на данный момент.
## Git branchwork
### Git branch 
Эта команда для осуществления просмотра имеющихся веток. Для создания новой ветки используется команда *git branch <имя новой ветки без скобок>* А для удаления веток используют команды:
* git branch -d (что удалит ветку при отсутствии конфликтов)
* git branch -D (удалит ветку в любом случае)
## Git merge
эта команда позволяет производить слияние двух веток в одну *git merge <имя ветки которую хотите присоеденить>* При этом присоединяет указанную ветку к той, на которой вы находитесь в данный момент.
### Удаленные репозитории
## Git clone
эта команда позволяет производить копирование из внешнего репозитория для дальнейшего редактирования.
## Git pull
эта команда позволяет производить скачивание актуальной версии файла из текущего удаленного репозитория и проводить автоматическое слияние с локальной версией при отсутствии конфликтов.
## Git push
эта команда позволяет отправить текущую версию файла в удаленный репозиторий(при первом использовании команды потребуется авторизация)
## Как предожить изменения чужому удалённому репозиторию?
1. Делаем форк (fork) интересующего нас аккаунта
2. Делаем *git clone* для нашей версии этого репозитория.
3. Создаём ветку с предложенными изменениями.
4. Производим изменения только в этой ветке.
5. Отправляем эти изменения на свой аккаунт *git push*
6. В окне на GitHub появляется возможность отправить pull request