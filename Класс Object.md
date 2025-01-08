Класс `Object` является суперклассом для всех классов в Java. Класс `Object` предоставляет методы, которые являются общими для всех объектов в Java, такие как `equals()`, `hashCode()`, `toString()`, `clone()` и другие.

Вот примеры использования некоторых методов класса `Object`:

1. Метод `equals()`:

```java
public class Main {
    public static void main(String[] args) {
        String str1 = "Hello";
        String str2 = "Hello";
        String str3 = new String("Hello");

        System.out.println(str1.equals(str2)); // true
        System.out.println(str1.equals(str3)); // true
        System.out.println(str1 == str3); // false
    }
}
```

В этом примере сравниваются два объекта `String` с помощью метода `equals()`. Обратите внимание, что сравнение с помощью оператора `==` дает разные результаты, потому что оператор `==` сравнивает ссылки на объекты, а не их содержимое.

2. Метод `hashCode()`:

```java
public class Main {
    public static void main(String[] args) {
        String str1 = "Hello";
        String str2 = "Hello";
        String str3 = new String("Hello");

        System.out.println(str1.hashCode()); // 69609650
        System.out.println(str2.hashCode()); // 69609650
        System.out.println(str3.hashCode()); // 69609650
    }
}
```

В этом примере вызывается метод `hashCode()` для трех объектов `String`. Метод `hashCode()` возвращает хэш-код объекта, который используется для поиска объекта в коллекциях, таких как `HashSet` и `HashMap`. Обратите внимание, что хэш-коды трех объектов одинаковы, даже если они созданы с помощью разных конструкторов.

3. Метод `toString()`:

```java
public class Main {
    public static void main(String[] args) {
        Object obj = new Object();
        System.out.println(obj.toString()); // java.lang.Object@15db9742

        String str = "Hello";
        System.out.println(str.toString()); // Hello
    }
}
```

В этом примере вызывается метод `toString()` для объекта `Object` и объекта `String`. Метод `toString()` возвращает строковое представление объекта. По умолчанию метод `toString()` возвращает строку, содержащую имя класса и хэш-код объекта. Для объектов `String` метод `toString()` возвращает содержимое строки.

4. Метод `clone()`:

```java
public class Main {
    public static void main(String[] args) throws CloneNotSupportedException {
        Employee emp1 = new Employee("John", 30);
        Employee emp2 = (Employee) emp1.clone();

        System.out.println(emp1.getName()); // John
        System.out.println(emp1.getAge()); // 30
        System.out.println(emp2.getName()); // John
        System.out.println(emp2.getAge()); // 30
        System.out.println(emp1 == emp2); // false
    }
}

class Employee implements Cloneable {
    private String name;
    private int age;

    public Employee(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public int getAge() {
        return age;
    }

    public Object clone() throws CloneNotSupportedException {
        return super.clone();
    }
}
```

В этом примере создается класс `Employee`, который реализует интерфейс `Cloneable`. Метод `clone()` вызывает метод `clone()` из класса `Object`, который создает копию объекта. Обратите внимание, что для вызова метода `clone()` необходимо реализовать интерфейс `Cloneable`.

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