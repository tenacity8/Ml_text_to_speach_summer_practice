# Работа с проектом

`vscode` при старте предложит установить рекомендованныек расширения - с ним лучше согласиться.


## Настройка окружения

### Python

Установите `python` для соответствующей операционной системы. 

**ВАЖНО** 

При установке в windows - укажите галочку - добавить python в переменную окружения `PATH`

### Pipenv

Мы используем виртуальное окружение `pipenv`, для его установки используйте следующую команду:

```shell
pip install pipenv
```
Установку требуется сделать только 1 раз, активацию - каждый раз когда вы перезапускаете терминал. 


Для активации виртуального окружения следует выполнить следующую команду, при этом выполнять ее нужно в каталоге текущего проекта `python` (рядом с текущим `README.md` файлом и содержит `Pipfile`)

```
pipenv shell
```

После этого необходимо установить зависимости, указанные в `pipenv` файле



После установки pipenv при использовании `vscode` следует выбрать версию интерпретатора, привязанный к проекту. Для этого можно выполнить следующую последовательность действий. Настраивать требуется только 1 раз при настройке виртуального окружения.

- Нажать комбинацию клавиш `ctrl-shift-p`
- Начать писать `Reload window`
- Начать писать `Python select interpreter`
- Выбрать на уровне рабочей области
- Найти свое окружение, скорее всего в его имени в скобках будет указано `(python-"НАБОР_СИМВОЛОВ")`

Ваше рабочее окружение настроено и можете его иcпользовать.

### Доступные команды

Команды проверок, запускаемые в `github actions` можно также запустить локально выполнением одной из следующих команд 

```shell
pipenv run test
pipenv run lint
pipenv run lintMyPy
```

Для работы необходимо скачать файлы с обученной моделью deepspeech и положить их в каталог models

Для запуска следует выполнить следующую команду
```
python mic_vad_streaming.py -m ../models/deepspeech-0.9.3-models.pbmm -s ../models/deepspeech-0.9.3-models.scorer
```

