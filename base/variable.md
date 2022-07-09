# Базовые понятия
## Понятие "Переменная"

**"Переменная"** - это имя, которое программист может дать значению.

Вот так вот просто. 

Давайте разберемся, что это за имя и для чего его нужно вообще давать?

Допустим, что мы написали программу, которая вычисляет возраст человека, зная его год рождения и текущий год:
```php
<?php

echo 2020 - 1980;
```
Здесь у нас 2020 - текущий год, а 1980 - год рождения. Программа совершенно ожидаемо выводит нам число `40`.

Однако, хотя программа и выполняет свою роль, она всё-таки написана неоптимально. Почему? 

Ну во-первых потому что вычисленное
значение потеряно! Да, мы вывели число 40, но что если, мы захотим его использовать снова? Мы никак не можем к нему 
обратиться, потому что после вычисления значения выражения это самое значение исчезло - нет никакого способа вновь его
использовать, кроме как написать снова `2020-1980`.

Во-вторых, давайте представим ситуацию, что нам нужно на основании года рождения человека вычислить не только его возраст,
но и какую-то другую величину - например узнать, сколько ему было лет в год проведения олимпиады в Сочи. Разумеется, 
мы можем написать еще одно выражение, `2014-1980` и получить результат. Но: сколько раз нам пришлось написать значение 
года рождения? Два? Значит вероятность ошибки выросла в два раза! А что если нам потребуется исправить год рождения, мы в 
одном месте программы это сделаем, а во втором забудем?

Все эти проблемы позволяют решить **переменные** - имена, которыми можно "назвать" значения.

## Присваивание

Для создания имени значения (то есть переменной) в PHP нужно написать знак `$`, сразу после него имя переменной, 
затем знак `=` и значение. Например,
так:

```php
<?php

$age = 2020 - 1980;
```

Эта операция называется **присваиванием**. Говорят, что мы "присвоили переменной `$age` значение выражения `2020-1980`".
Такой термин, конечно, не очень корректный, потому что первично всё-таки значение, а не имя переменной. Сначала мы 
вычисляем значение, а затем даем ему имя, а не наоборот.

> Кстати, а какими могут быть имена переменных? В PHP - практически любыми, главное - не забывать знак `$`. Вы можете назвать
переменную по-русски (`$возраст`) или даже по-китайски (`$年龄`), но, конечно, лучше так не делать. Пожалуйста, используйте
для имён переменных латинские буквы и цифры, причем всегда начинайте имя с буквы. Еще можно использовать `_` - знак
подчеркивания.

## Использование переменных

Переменная затем может быть использована в любом контексте, в котором может быть использовано само значение.

К примеру, можно вывести ее значение:

```php
<?php

$age = 2020 - 1980;
echo $age;
```

Или использовать в расчетах значений выражений:

```php
<?php

$wasBornIn = 1980;
$currentAge = 2020 - $wasBornIn;
$sochiAge = 2014 - $wasBornIn; 
```


## Словарик

| Русский термин | Английский термин |
| --- | --- |
| переменная | variable |
| возраст | age |
| текущий | current |