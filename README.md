## Разворачивание виртуального окружения

Когда у вас уже есть Pipfile и Pipfile.lock и вам нужно установить все пакеты в новое (чистое) виртуальное окружение, вы можете выполнить:

    pipenv install — для установки самых свежих версий пакетов из Pipfile в окружение с возможным обновлением Pipfile.lock (если вышли более новые версии пакетов, чем указанные в Pipfile.lock).
    pipenv install --dev — то же самое, но установятся также пакеты, помеченные как --dev, для разработки.
    pipenv sync установит строго указанные в Pipfile.lock версии пакетов и не будет проверять наличие более свежих версий.
    pipenv install --deploy установит версии строго такие, как указано в Pipfile.lock и, если хеши пакетов не совпадут с хешами из Pipfile.lock, или версия Python не совпадает, выдаст ошибку и прекратит установку.
    pipenv install --system — то же, что и pipenv install, но установит пакеты глобально в систему, а не в виртуальное окружение.