В Java, ключевые слова `throw` и `throws` используются для работы с исключениями.

1. Ключевое слово `throw` используется для явного выброса исключения в коде. Вот пример:

```java
public class Main {
    public static void main(String[] args) {
        int age = -5;
        if (age < 0) {
            throw new IllegalArgumentException("Age cannot be negative");
        }
        System.out.println("Age is: " + age);
    }
}
```

В этом примере, если переменная `age` оказывается меньше 0, выбрасывается исключение `IllegalArgumentException` с сообщением об ошибке.

2. Ключевое слово `throws` используется для объявления исключений, которые может выбросить метод. Вот пример:

```java
import java.io.FileNotFoundException;
import java.io.FileReader;

public class Main {
    public static void main(String[] args) {
        try {
            readFile("non-existing-file.txt");
        } catch (FileNotFoundException e) {
            System.out.println("File not found: " + e.getMessage());
        }
    }

    public static void readFile(String fileName) throws FileNotFoundException {
        FileReader reader = new FileReader(fileName);
        // code to read file
    }
}
```

В этом примере, метод `readFile` объявлен с использованием `throws FileNotFoundException`, так как он может выбросить исключение `FileNotFoundException`, если файл не найден. Метод `main` обрабатывает это исключение в блоке `catch`.

Использование `throws` позволяет передать обработку исключений на уровень выше, что может быть полезно, если метод не может или не должен обрабатывать исключение самостоятельно.

Важно отметить, что исключения, выброшенные с помощью `throw`, должны быть обработаны с помощью `try-catch` или объявлены с помощью `throws`. Если исключение не обработано, программа завершится с ошибкой.

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
