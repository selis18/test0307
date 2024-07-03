# test0307

1. Какой будет результат выполнения php-кода?

```
<?php
$a = '123456';
$a[$a[1]] = '2';
echo $a
```

```
Ответ: 122456
```

2. Какой будет результат выполнения php-кода?

```
<?php
$item = 5;
$list = [1, 2, 3];
foreach ($list as $item) {
 $item++;
}
echo $item;
```

```
Ответ: 4
```

3. Какой будет результат выполнения кода?

```
<?php
class A {
 public $foo = 1;
}
$a = new A();
$b = $a;
$b->foo = 2;
echo $a->foo
```

```
Ответ: 2
```

4. Какой будет результат выполнения php-кода?
```
<?php

interface Foo {
 const A = 'Foo';
}
class Bar implements Foo {
 const A = 'Bar';
}
echo Bar::A;
```

```
Ответ: Bar
```

5. Какой будет результат выполнения php-кода?

 ```  
<?php
trait Foo {
 public function getName() {
 echo "Foo\n";
 }
}
class Bar {
 public function getName() {
 echo "Bar\n";
 }
}
class Baz extends Bar {
 use Foo {
 getName as private;
 }
}
$baz = new Baz();
$baz->getName();
```

```
Ответ: Ошибка доступа к методу. В trait Foo метод getName публичный, но в классе Baz пытаются использовать его как приватный. Без этого фактора было бы выведено "Foo\n"
```

6. Какой будет результат выполнения js-кода?

```
const users = {
 data: [
 {name: 'John Smith'},
 {name: 'Ellen Simons'}
 ],
2
 showFirst: function (event) {
 console.log(this.data[0].name);
 }
}
$('button').click(users.showFirst);

```

```
Ответ: John Smith
```

7. Что означает данная конструкция

```
const a = {...b, ...c};
```

```
Ответ: Объединение объекта a и b путём сложения всех их свойства в один объект а. 
      Если свойства будут одинаковые, то значения будут из последнего объекта.
```

8. В таблице Article 100 млн. записей, в Category – 200. Напишите sql-запрос для выбора всех статей в не скрытых разделах.
```
Таблица Article
article_id int(10)
title varchar(100)
category_id int(10)
Таблица Category
category_id int(10)
title varchar(100)
hidden int(1)
```
```
Ответ: SELECT * FROM Article WHERE category_id IN (SELECT category_id FROM Category WHERE hidden = 0);
```

9. Какой будет результат выполнения запроса SELECT count(id) FROM table1 в MySQL ? Таблица table1 имеет вид:

```
| id | title |
| --- | --- |
| 0 | title0 |
| 1 | title1 |
| 2 | title2 |
| NULL | title3
```
```
Ответ: 3. Строка с NULL не учитывается.
```

10. С помощью какой команды можно посмотреть план выполнения запроса в MySQL?
```
Ответ: Explain
```

11. Какой паттерн проектирования необходимо использовать для реализации класса, который должен иметь только одну сущность во время выполнения скрипта?
```
Ответ: Singleton
```

12. Что такое AWK?
```
Ответ: Скриптовый язык для терминала. Используется для работы с текстовыми данными.
```
