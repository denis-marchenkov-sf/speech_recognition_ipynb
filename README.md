# Распознавание речи

![Python](https://img.shields.io/badge/python-3670A0?logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/jupyter-%23FA0F00.svg?logo=jupyter&logoColor=white)
![SkillFactory](https://img.shields.io/badge/-SkillFactory-green)

<img src="https://raw.githubusercontent.com/denis-marchenkov-sf/assets/master/works_on_my_machine.png" width="100" height="100" />

<br/>

## Оглавление

[ Описание](#описание)

[ Пример работы](#пример-работы)

[ Описание интерфейса](#описание-интерфейса)

[ Порядок запуска](#порядок-запуска)

<br/>

## Описание

Реализована функция распознавания речи на русском языке в текст.

Реализация осуществлена в .ipynb файле c графическим интерфейсом на базе ipynb-совместимых виджетов.

Поддерживается возможность записывать аудиофайлы, загружать аудиофайлы в формате .wav и распознавать речь в режиме реального времени.

Текстовые расшифровки сохраняются в формате .txt в рабочую директорию, аудиозаписи сохраняются в формате .wav

Поскольку западные сервисы дружно заблокировали всем нам доступ, а яндекс-cloud не позволяет создавать биллинг физлицам из братской Беларуси - была выбрана офлайн модель распознавания речи **Vosk**.

<br/>

## Пример работы

![speech](https://raw.githubusercontent.com/denis-marchenkov-sf/assets/master/speech_record_demo.gif)

<br/>

## Описание интерфейса

Графический интерфейс состоит из двух блоков: "Запись" и "Распознавание"

Блок **"Запись"** содержит виджет выбора директории для сохранения аудиозаписи (по умолчанию рабочая директория) и непосредственно кнопку записи аудио:

![record](https://raw.githubusercontent.com/denis-marchenkov-sf/assets/master/recording.png)

Блок **"Распознавание"** содержит виджет выбора существующего .wav файла, кнопку распознавания выбранного файла, кнопку распознавания речи на лету и текстовое поле с результатом:

![regognize](https://raw.githubusercontent.com/denis-marchenkov-sf/assets/master/recognition.png)

<br />

## Порядок запуска

Запуск исключительно из-под VsCode на Windows 10. За другое поручиться не могу.

При тестировании на виртуальной машине запись звука работать не будет. А может и на вашей не будет :( 

Для VsCode необходимы расширения: python, jupyter, ipykernel.

Необходимые пакеты:
```
! pip install ipywidgets
! pip install IPython
! pip install ipyfilechooser
! pip install wave
! pip install vosk
! pip install pydub
! pip install torch
! pip install transformers
! pip install pyaudio
```
После установки пакетов из ячейки .ipynb-ноутбука или VsCode-терминала - VsCode необходимо перезагрузить.

Склонировать репозиторий ``` https://github.com/denis-marchenkov-sf/speech_recognition_ipynb.git ```. Репозиторий содержит несколько примеров .wav файлов в папке **samples**.

Открыть папку репозитория в VsCode. Открыть ipynb-ноутбук **speech_recognition.ipynb**, запустить выполнение всех ячеек. В процессе выполнения будет создан подкаталог speech_recognition, в который будет скачана и распакована языковая модель Vosk.

По завершению выполнения всех ячеек (и если звёзды сойдутся в правильном порядке и на чужой машине всё заработает) в последней ячейке ноутбука отобразится графический интерфейс (см. [пример работы](#пример-работы))

**Внимание**: размер архива языковой модели - около 1.5 GB



[к оглавлению](#оглавление)
