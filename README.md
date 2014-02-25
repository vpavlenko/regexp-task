Регулярные выражения
====================

[Статья про регулярные выражения в Питоне](http://blog.dzinko.org/2011/03/python.html)

[Один из сервисов по отладке регулярных выражений](http://regex101.com/#python) - при использовании в поле "flags" справа от поля регулярного выражения напишите "g" (будет искать все вхождения, а не только первое)


Задания
=======

Каждое задание оценивается в 7 баллов, задания высылаются на почту [vpavlenko.int@gmail.com](mailto:vpavlenko.int@gmail.com)


Задание 1 (в классе)
--------------------

Напишите регулярное выражение, которое находит весёлые смайлики и не находит грустных.

Весёлые: :-), :), (:, (-:, :D, :-P, ;) и прочее

Грустные: :(, :c, :-/, )% и прочее


Задание 2 (на дом)
------------------

В файле [usa.txt](usa.txt) находится статья "United States" из английской википедии.

1. Сколько раз в ней встречаются номера источников в квадратных скобках? года? денежные суммы? проценты?
2. Напишите программу, которая находит в этом файле все вышеперечисленные объекты и выписывает их.


Задание 3 (на дом)
------------------

В файле [words.txt](words.txt) находится краткий орфографический словарь английского языка.

1. Сколько слов начинаются на согласную букву, за которой следует гласная?
2. Сколько слов имеет три гласных буквы, идущие подряд? Сколько слов имеет три согласных буквы, идущие подряд?
3. Сколько слов имеет три гласных буквы, идущие подряд, и не заканчивается на `'s`?

Минутка магии
=============

    >>> re.sub('(\d{1,2})/(\d{1,2})/(\d{4})', lambda x: '{1}.{0}.{2}'.format(*x.groups()), '02/22/2014, trash, 07/23/1998') 
    '22.02.2014, trash, 23.07.1998'
