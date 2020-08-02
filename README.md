## Написать 2 пайплайны в Jenkins CI:
1.    Сборка докер имеджа и пуш на свой аккаунт на докер хабе (https://hub.docker.com). Должно быть 2 или больше джобы (job)
Прикладываю описание: 
Ubuntu 20.04 latest (light) – создать двух пользователей: админ с широкими привелегиями, пользователь для nginx (start, stop, restart). Установить: java, nginx, nettools.
Файл конфигурации для nginx должен быть создан и сконфигурирован вне контейнера (в папке рядом с Dockerfile), поменять порт 80 на любой другой, например 8080. Другие параметры меняйте по вашему усмотрению.
Протестировать  работу вашего контейнера отдельным стейджем после сборки (в той же пайплайне) "постучавшись" на порт nginx. Т.е. curl/wget проверить соединение в райнтайме (или любой другой способ).
Любые ваши дополнения или улучшения приветствуются.



![Screenshot_20200803_013758.png](/images/Screenshot_20200803_013758.png)



![Screenshot_20200803_013824.png](/images/Screenshot_20200803_013824.png)



![Screenshot_20200803_013837.png](/images/Screenshot_20200803_013837.png)



2) Сборка и тестирование  проекта (Java, JS, etc.). Должно быть 2 или больше джобы (job):
- Собрать проект из любого Git репозитория.
- Протестировать работу приоложения (продемострировать работу собранного приложения в выбранной вами среде).


![Screenshot_20200802_193814.png](/images/Screenshot_20200802_193814.png)



![Screenshot_20200802_193839.png](/images/Screenshot_20200802_193839.png)

