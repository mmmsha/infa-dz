# Команда grep
Команда grep - это инструмент поиска текста в файлах и потоках данных. Она позволяет находить строки, соответствующие заданному шаблону, и выводить их на экран или сохранять в файл.
### Синтаксис команды
grep [опции/флаги] [текст, который нужно найти] [название файла]
Опции необязательны. Если их нет, то, например, строка `grep "hello" file.txt` будет искать строки, содержащие слово hello, в файле под названием file.txt
## Примеры
Вот несколько основных опций с примерами их использования:
* `grep -i "hello" file.txt` (поиск без учета регистра)
* `grep -v "hello" file.txt` (поиск строк, которые не содержат слово hello)
* `grep -n "hello" file.txt` (поиск с выводом номера строки)
* `grep -C5 "hello" file.txt` (поиск с выводом контекста - 5 строк до и после совпадения)

grep также может искать совпадения сразу в нескольких файлах. Например, `grep "hello" file1.txt file2.txt`

В grep также есть реуглярные выражения для текста. Вот примеры некоторых из них:
* `grep "^hello" file.txt` (поиск строк, начинающихся с hello)
* `grep "hello$" file.txt` (поиск строкк, заканчивающихся на hello)
* `grep "a-z" file.txt` (поиск в диапазоне символов от a до z)

## Пример задания
1. Создайте текстовый файл example.txt с следующим содержимым:  
>Hello, world!  
This is a test file.  
It contains multiple lines of text.  
Some lines contain the word 'test'.  
Others do not.
3. Используйте команду grep для поиска строк, содержащих слово "test": `grep "test" example.txt`
4. Теперь найдите строки, которые не содержат слово "test": `grep -v "test" example.txt`
5. Используйте опцию -i для поиска строк, содержащих слово "test" без учета регистра: `grep -i "TEST" example.txt`

## Задание
1. Создайте файл data.txt со следующим текстом:  
> This is a sample text file for testing the grep command.  
The file contains multiple lines with different keywords.  
Line 3 contains the word error.  
Line 4 has no special keywords.  
Here is another error on line 5.  
Warning: this is a warning message.  
Line 7 contains the word INFO in uppercase.  
Line 8 has the word info in lowercase.  
Debug information can be found on line 9.  
Line 10 contains the word debug again.  
Line 11 has the word "errors" (plural).  
Line 12 contains "warn" but not "warning".  
Line 13 has "Info" with a capital I.  
Line 14 contains "debugging" as a part of the word.  
Line 15 has "ERROR" in uppercase.  
Line 16 contains "no-keyword" but no special words.  
Line 17 has "info" followed by "information".  
Line 18 contains "debug" and "error" together.  
Line 19 has "WARNING" in uppercase.  
Line 20 contains "infographic" (partially matches "info").  
2. Используйте команду grep для выполнения следующих задач:
  * Найдите все строки, содержащие слово "error" (в любом регистре), и сохраните результат в файл errors.txt
  * Найдите все строки, не содержащие слово "warning" (в любом регистре), и сохраните результат в файл no_warning.txt
  * Найдите все строки, содержащие слово "info" (в любом регистре), но не "information", и сохраните результат в файл only_info.txt
  * Выведите номера строк, содержащих слово "debug" (в любом регистре), включая частичные совпадения, и сохраните результат в файл debug_and_more.txt
  * Найдите все строки, содержащие слово "error" или "warning" (в любом регистре)
  * Найдите все строки, содержащие слово "info" (в любом регистре), и выведите их с номерами строк
3. Приложите в отчете скриншоты терминала и содержимого файлов

## Ссылки на материалы
1. https://habr.com/ru/companies/itsumma/articles/492932/#5
2. [Документация по команде grep](https://www.gnu.org/software/grep/manual/grep.html)
3. https://www.geeksforgeeks.org/grep-command-in-unixlinux/
4. https://wiki.merionet.ru/articles/16-poleznyh-primerov-grep


