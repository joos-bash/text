# text
Текстовые утилиты

Утилиты для просмотра текстовых файлов
- cat (concatenate) - cat [файл...] - читает содержимое одного или нескольких файлов и копирует его в стандартный вывод
- less - less -N file - позволяет пронумеровать строки
- head - Выводит первые 10 строк из текстового файла
- tail - Выводит последние 10 строк из текстового файла
- tail -f - позволяет следить за обновлением файла в режиме реального времени

Сортировка текстовых файлов
- sort - сортирует все указанные файлы, результат сортировки файлов отправляется на стандартный вывод
- sort [параметр] ... [файлы]
- -b - Пробелы в начале сортируемых полей или в начале ключей будут игнорироваться
- -d - При сортировке будут игнорироваться все символы, кроме букв, цифр и пробельных символов
- -f - Игнорирование регистра букв
- -r - Сортировка в обратном порядке
- -o файл - Вывод результатов сортировки в файл
- -t символ - Использование указанного символа в качестве разделителя полей
- -n - Сортировка числовых значений
- -h - Сортировка удобочитаемых цифр: 2K 1G 100M
- -k - Сортировка по указанному диапазону столбцов
- -u - Убрать повторы — аналог команды uniq

Разбивка файла
- split - используется для разделения файлов на части
- wc (word count) - используется для подсчёта слов в файле
  - wc -l /var/log/messages - Для подсчёта строк в текстовом файле
  - wc -c /var/log/messages - Для подсчёта байтов в текстовом файле
  - wc -l -w -L — вывести длину самой длинной строки
- cut - используется для извлечения фрагментов текста из строк и вывода их в стандартный вывод. может принимать имена файлов в аргументах или данные со стандартного ввода
- -c - Cписок символов: --characters=     Извлекает фрагмент строки, определяемый списком символов. Список может включать один или несколько числовых диапазонов, разделённых запятыми
- -f - Cписок полей: -fields=      Извлекает одно или несколько полей из строки, как определено аргументом списка символов. Список может включать одно или несколько полей или диапазонов полей, разделённых запятыми
- -d - Символ-разделитель: --delimiter=     В присутствии параметра -f в качестве разделителя полей используется символ-разделитель. По умолчанию поля должны отделяться друг от друга одним символом табуляции --complement. -d извлекает строку текста целиком, кроме фрагментов, определяемых параметром -c и/или -f
- cut -c1-3 /etc/passwd — диапазон символов
- cut -d':' -f1 /etc/passwd

Утилиты для поиска
- find - утилита для сложного поиска файлов. В простейшем случае программе find можно передать одно или несколько имён каталогов для поиска
- find /tmp | wc -l
- find ~ -type d | wc -l
- find ~ -type f | wc -l
- find ~ -type f -name "*.JPG" -size +1M | wc -l
- find /tmp -type f -size +5M -mtime +3 -delete
- locate - утилита для поиска файлов по имени в Linux. Выполняет быстрый поиск в базе данных имён файлов и выводит все имена, соответствующие искомой строке
- Locate -e — существующие файлы

Текстовые редакторы
- Vim — свободный текстовый редактор, созданный на основе более старого vi
- Режим вставки - Осуществляется редактирование текста
- Командный режим - Выполняется ввод специальных команд для работы с текстом
- :q! - Выйти без сохранения
- :w - Сохранить изменения
- :w <файл> - Сохранить изменения под именем <файл>
- :wq - Сохранить и выйти
- :q - Выйти, если нет изменений
- i - Перейти в режим вставки символов в позицию курсора
- a - Перейти в режим вставки символов в позицию после курсора

- nano — консольный текстовый редактор
- Ctrl + G - Подсказка по горячим клавишам
- Ctrl + X - Выйти из nano
- Ctrl + O - Сохранить файл
- Ctrl + W - Поиск
- Ctrl + \ - Замена
- Ctrl + K - Вырезать строку
- Ctrl + U - Вставить строку
- Alt + U - Отменить последнее действие
- Alt + E - Отменить последнее действие






