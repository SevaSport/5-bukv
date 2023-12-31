# Проект подбора слов для игры 5 букв
[_Игра 5 букв Тинькофф_](https://5bukv.tinkoff.ru/)

## Использование
Основной файл help.js, который запускается с определенными параметрами, которые могут комбинироваться.

### Указание букв, содержащихся в слове
```sh
node help.js +а +б +в
```

### Указание букв, исключаемых из слова
Буквы, которые необходимо исключить из слова указываются после символа минус (-а -б)
```sh
node help.js -а -б -в
```

### Задание конкретных позиций букв в слове
Позиция букв указываются в человекопонятном формате, начиная с 1.
```sh
node help.js 1а 2б 3в
```

### Комбинация параметров
Параметры можно комбинировать.
```sh
node help.js +с 4в -д -у -н -т -я -о -ь
```

## Технические требования к словарю

> Note: Словарь который использует скрипт help.js лежит в той же директории с именем rus-5.txt.

Словарь содержит слова в формате txt и кодировки utf8 без BOM.

Каждое слова распологается на одной строке.

Разделителем строк используется управляющая последовательность \n.

## Конвертирование словаря
Для создания словаря из 5 букв используется срипт migrator.js. 

Сприпт принимает 2 параметра: исходный файл и целевой файл словарей.

### Создание словаря
```sh
node migrator.js russian_nouns.txt rus-5.txt
```