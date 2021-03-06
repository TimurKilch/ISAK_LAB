# ISAK_2
## Усенко Д.Е. М3О-312Б-18.

### Постановка задачи
1. Выведите на экран листинг характеристик (в длинном и коротком форматах) процессов, инициализированных с Вашего терминала. Проанализируйте и объясните содержание каждого поля сообщения.
2. Выведите на экран листинг характеристик всех процессов. Используйте при необходимости конвейер с more для постраничного просмотра листинга. Какой процесс является родительским для большинства процессов? Что означает символ ? в поле управляющий терминал процесса?
3. Выведите на экран листинг процессов, запущенных конкретным пользователем. Какой ключ пришлось использовать? Что говорит значение ? в поле управляющий терминал процесса?
4. Разработайте и запустите простейшую процедуру в фоновом режиме с бесконечным циклом выполнения, предусматривающую, например, перенаправление вывода каких-то сообщений в файл или в фиктивный файл, и использующую команду sleep для сокращения частоты циклов процедуры.
5. Выполните п. 1. Объясните изменения в листинге характеристик процессов.
6. Понизьте значение приоритета процедуры. На что и как повлияет эта операция при управлении вычислительным процессом системы? Как отразятся ее результаты в описателях процессов?
7. Проанализируйте листинг процессов. Какой процесс является родительским для процедуры.
8. Выйдите из системы и войдите заново. Проанализируйте листинг процессов. Объясните изменения в системе.
9. Запустите процедуру в фоновом режиме, но предусмотрите ее защиту от прерывания при выходе из системы.
10. Выполните п.6. Объясните изменения PPID процедуры.
11. Завершите выполнение процесса процедуры.
12. Запустите процедуру в интерактивном режиме с перенаправлением вывода в соответствующий файл.
13. Переведите задание с процедурой в фоновый режим и проанализируйте сообщение на экране. Что пришлось дополнительно сделать? Как выглядят приостановленные процессы в листинге команды ps?
14. Переведите задание с процедурой в интерактивный режим и проанализируйте сообщение на экране.
15. Завершите выполнение процедуры и проанализируйте сообщение на экране

### Практическая часть:

1. Выводим в окно терминала листинг характеристик процессов в коротком формате 
![Screenshot](/lab2/Screenshot_1.png)
Поле PID означает идентификатор процесса. Поле TTY означает имя иерминала с которого запущен процесс. Поле TIME означает процессорное время, затраченное на выполнение данного процесса. Поле CMD означает команду которая вызвала выполнение процесса
Выведем на окно терминала листинг характеристик процессов в длинном формате:
![Screenshot](/lab2/Screenshot_2.png)
Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса. Вывод дополнился новыми полями. Поле UID означает идентификатор пользователя, который запустил процесс. Поле PPID означает идентификатор родительского процесса. Поле STIME означает время старта процесса.
2. Выводим листинг характеристик всех процессов при помощи команды ps ax -f:
![Screenshot](/lab2/Screenshot_3.png)
3. Чтобы вывести листинг процессов для определенного пользователя, выйдем из пользователя "root" 
![Screenshot](/lab2/Screenshot_4.png)
4. Воспользуемся редактором "vi" и создадим программу с помощью команды "vi s.py": Перейдем в режив ввода нажатием клавиши "i" и введем текст программы:
![Screenshot](/lab2/Screenshot_5.png)
Сохраним и выйдем из редактора
Запустим программу из терминала в фоновом режиме: [root@localgost dimausenko]# python sl.py & 
5. Выведем листинг характеристик процессов root@localgost dimausenko]# ps -f
![Screenshot](/lab2/Screenshot_6.png)
6. Понизим приоритет процесса 1265 до значения 5 и выведем характеристику процессов с ключом "l":
![Screenshot](/lab2/Screenshot_7.png)
![Screenshot](/lab2/Screenshot_8.png)
7. Родительским процессом для процесса 1251 является процесс с идентификатором 1247 - bash.
8. Выйдем из системы командой "exit" и зайдем заново 
9. Запустим процедуру в фоновом режиме и предусмотрим ее защиту от прерывания.
![Screenshot](/lab2/Screenshot_9.png)
10. Выведим листинг характеристик процессов
![Screenshot](/lab2/Screenshot_10.png)
11. Завершим выполнение процесса процедуры сигналом "-9":
![Screenshot](/lab2/Screenshot_11.png)
12. Запустим процедуру в фоновом режиме а затем переведем ее в интерактивный режим.
![Screenshot](/lab2/Screenshot_12.png)
![Screenshot](/lab2/Screenshot_13.png)
13. Приостановим выполнение процесса сочетанием клавиш Ctrl + z. 
![Screenshot](/lab2/Screenshot_13.png)
![Screenshot](/lab2/Screenshot_14.png)
14. Переведем процедуру в интерактивный режим:
[root@localgost dimausenko]#fg 
```sh
python s.py
```
15. Завершим выполнение процесса с помощью команды kill. 
![Screenshot](/lab2/Screenshot_15.png)

Вывод: В ходе лабораторной работы были изучены команды для работы с процессами в операционной системе Linux, а так же проведена работа с текстовым редактором vi.
