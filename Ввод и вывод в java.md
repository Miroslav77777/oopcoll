## Ввод

Для ввода данных предусмотрен класс Scanner, который содержит определенные методы для чтения различных данных. Чтобы организовать ввод с клавиатуры необходимо создать экземпляр класса Scanner и связать его со стандартным входным потоком System.in

```java
Scanner sc = new Scanner(System.in)
```

**Методы**

-nextInt() чтение целого
-nextDouble() чтение вещественного 
-nextLine() чтение строки
-next()

```java 
int a = sc.nextInt();
```

## Вывод

Для организации вывода предусмотрен класс System у которого имеется объект out с двумя методами для вывода print(на одной строке) и println

```java
System.out.print(“Hello world”);
System.out.println(“Hello world”);

int a = 10;
System.out.println(“a = ” + a);
```

## Ссылки на другие вопросы

[[Характерные особенности языка Java]]
[[Типы данных]]
[[Объявление переменных и констант]]
[[Основные операции]]
[[Основные операторы]]
[[Ввод и вывод в java]]
[[Классы (основные понятия)]]
[[Классы (конструктор, совмещенные методы и вся хуйня)]]
[[Модификаторы доступа]]
[[Наследование]]
[[Полиморфизм]]
[[Абстрактные классы]]
[[Интерфейсы]]
[[Исключения]]
[[Исключения (try, catch, finally)]]
[[Исключения(trow, throws)]]
[[Класс Object]]
[[Геттеро, сеттеро, два ствола]]