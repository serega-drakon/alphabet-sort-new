## Павелу Филипенко

Для простоты проверки я выкинул кучу мусора из проекта, упростил комменты и убрал лишние функции. Рекомендую проверять "Release" тк там меньше кода и легче ориентироваться :)
Комментарии к каждой функции, если ее смысл неочевиден есть, единственное я в одном месте все заточил под кодировку ASCII, ввел не 'a', а её численное представление, у меня чего-то компилятор неправильные значения знаковым символам дает.

_Поддержку буквы Ё я так и не добавил, сделать это очевидно, но дрочно. Ну в поэме почему-то её вообще нету)_

# Alphabet sort

Данная программа выполняет сортировку всех строк текста в алфавитном порядке.

## Структура проекта

Проект состоит из двух версий программы : __Debug__ и __Release__. Вторая отличается от первой отсутствием проверок на ошибки и она рекомендуется к использованию, в силу более быстрого исполнения. В каждой соответствующей папке лежит:

- _main.c_ содержащий основной алгоритм сортировки
- Папка _include_, в которой находятся все библиотеки
- Библиотека _int_array_2d.h_, которая занимается созданием двумерного массива целых чисел и определением операций для него
- Библиотека _fileio.h_ в которой я собрал то, что не смог засунуть в предыдущую типа функции получения строки из файла
- Файлы ввода/вывода _main_in.txt_ и _main_out.txt_ в кодировке "Windows 1251 Cyrillic".

## Как это использовать? 

Необходимо в файл __main_in.txt__ поместить текст, который нужно отсортировать, при этом закодировав его в кодировке, которую поддерживает библиотека Си - _stdio.h_, гарантированно сработает кодировка "Windows 1251", поэтому используйте её. __Запускайте программу__, по итогу работы она сохранит отсортированную версию в __main_out.txt__. Готово!

## Инструкция по сборке

Собрать можно почти в любом компиляторе Си под вашу систему, думаю описывать это не нужно. Внешняя консоль не понадобится в силу того, что ввод/вывод программы совершается через файлы.


