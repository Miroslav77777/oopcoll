- Интерфейс `MouseListener` в Java предоставляет механизм для обработки событий, связанных с мышью.
- Классы, реализующие этот интерфейс, получают уведомления о событиях мыши, таких как нажатие, отпускание кнопки, вход и выход курсора мыши из компонента.

**Методы:**

- **`void mouseClicked(MouseEvent e)`:** вызывается, когда пользователь щелкает кнопку мыши.
- **`void mousePressed(MouseEvent e)`:** вызывается, когда пользователь нажимает кнопку мыши.
- **`void mouseReleased(MouseEvent e)`:** вызывается, когда пользователь отпускает кнопку мыши.
- **`void mouseEntered(MouseEvent e)`:** вызывается, когда курсор мыши входит в компонент.
- **`void mouseExited(MouseEvent e)`:** вызывается, когда курсор мыши выходит из компонента.

**Пример:**

```java
import java.awt.event.MouseEvent;
import java.awt.event.MouseListener;
import javax.swing.JFrame;
import javax.swing.JLabel;

public class MouseListenerExample extends JFrame implements MouseListener {

    private JLabel label;

    public MouseListenerExample() {
        super("MouseListener Example");
        setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        setSize(300, 150);
        setLayout(null);

        label = new JLabel("Click me!");
        label.setBounds(50, 50, 100, 30);
        label.addMouseListener(this);

        add(label);
        setVisible(true);
    }

    @Override
    public void mouseClicked(MouseEvent e) {
        label.setText("You clicked me!");
    }

    @Override
    public void mousePressed(MouseEvent e) {
        label.setText("Mouse pressed");
    }

    @Override
    public void mouseReleased(MouseEvent e) {
        label.setText("Mouse released");
    }

    @Override
    public void mouseEntered(MouseEvent e) {
        label.setText("Mouse entered");
    }

    @Override
    public void mouseExited(MouseEvent e) {
        label.setText("Mouse exited");
    } }
```

**В этом примере:**

- Класс `MouseListenerExample` наследует `JFrame` и реализует интерфейс `MouseListener`.
- Методы интерфейса переопределяются для обработки различных событий мыши.
- При взаимодействии с меткой (`JLabel`) изменяется текст в зависимости от действия пользователя с мышью.