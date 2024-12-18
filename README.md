# TodoManager для Sublime Text

**TodoManager** — это плагин для Sublime Text, который помогает организовать задачи, помеченные с помощью ключевых слов, в файлах. Он собирает все задачи из открытых файлов, фильтрует их по приоритету и ключевым словам, а также позволяет быстро переходить к нужным строкам.

## Установка

1. Убедитесь, что у вас установлен Sublime Text.
2. Установите плагин **TodoManager** с помощью [Package Control](https://packagecontrol.io/).
   
   Для этого:
   - Откройте Sublime Text.
   - Перейдите в `Tools > Command Palette`.
   - Введите `Package Control: Install Package` и нажмите Enter.
   - Найдите и выберите `TodoManager`.

## Конфигурация

После установки плагин будет искать задачи с ключевыми словами, заданными в конфигурационном файле. Чтобы настроить ключевые слова и их приоритеты:

1. Перейдите в `Preferences > Package Settings > TodoManager > Settings`.
2. Внесите изменения в файл настроек (например, добавьте или измените ключевые слова и их приоритеты).

Пример конфигурации:

```json
{
    "keywords": {
        "TODO": 1,
        "FIXME": 2,
        "TODO COMMENT": 3
    }
}
```

## Как использовать

### Просмотр задач

1. Откройте любой файл, в котором вы используете ключевые слова для пометки задач.
2. Перейдите в `Tools > TodoManager > Show Todo List` или используйте команду через командную палитру (`Ctrl+Shift+P` или `Cmd+Shift+P`), набрав `TodoManager: Show Todo List`.
3. Плагин соберет все задачи из открытых файлов и отобразит их в виде списка с приоритетами.

### Фильтрация задач

После того как список задач будет собран, вы можете фильтровать задачи по ключевым словам:

1. В появившемся списке задач выберите ключевое слово или выберите "All" для отображения всех задач.
2. Задачи будут отсортированы по приоритету, с возможностью просмотра описания каждой задачи.

### Переход к задаче

Для перехода к строке с задачей:

1. После фильтрации задач выберите нужную задачу в списке.
2. Плагин откроет соответствующий файл и переместит курсор на строку с задачей.

## Описание приоритетов

Задачи сортируются по приоритету, который можно настроить:

- **1** — Critical (Критический)
- **2** — High Priority (Высокий приоритет)
- **3** — Medium Priority (Средний приоритет)
- **4** — Low Priority (Низкий приоритет)
- **5** — Minor (Неважный)

Если приоритет не указан в тексте задачи, то используется значение по умолчанию из конфигурации.

## Примечания

- Плагин поддерживает любые открытые файлы в Sublime Text.
- Задачи ищутся только в текстовых строках, содержащих ключевые слова из конфигурации.
- Приоритеты могут быть указаны в квадратных скобках рядом с текстом задачи, например: `TODO [1] Исправить ошибку в коде`.

## Ссылки

- [Документация Sublime Text API](https://www.sublimetext.com/docs/api_reference.html)
- [Package Control для установки плагинов](https://packagecontrol.io/)

