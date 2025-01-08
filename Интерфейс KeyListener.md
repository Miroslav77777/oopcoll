
- Интерфейс `KeyListener` в Java предоставляет методы для обработки нажатия, отпускания и нажатия клавиш.
- Используется для создания событий, которые срабатывают, когда пользователь нажимает клавишу на клавиатуре.
- Методы интерфейса:
    - **`keyPressed(KeyEvent e)`**: срабатывает, когда клавиша нажата.
    - **`keyReleased(KeyEvent e)`**: срабатывает, когда клавиша отпущена.
    - **`keyTyped(KeyEvent e)`**: срабатывает, когда клавиша нажата и отпущена, генерируя символ.

**Пример кода:**

```java
import java.awt.event.*;
import javax.swing.*;

public class KeyListenerExample implements KeyListener {

    private JLabel label;

    public KeyListenerExample() {
        JFrame frame = new JFrame("KeyListener Example");
        label = new JLabel("Press any key");
        frame.add(label);
        frame.addKeyListener(this);
        frame.setSize(300, 100);
        frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        frame.setVisible(true);
    }

    @Override
    public void keyPressed(KeyEvent e) {
        label.setText("Key pressed: " + KeyEvent.getKeyText(e.getKeyCode()));
    }

    @Override
    public void keyReleased(KeyEvent e) {
        label.setText("Key released: " + KeyEvent.getKeyText(e.getKeyCode()));
    }

    @Override
    public void keyTyped(KeyEvent e) {
        label.setText("Key typed: " + e.getKeyChar());
    }

    public static void main(String[] args) {
        new KeyListenerExample();
    }
}
```