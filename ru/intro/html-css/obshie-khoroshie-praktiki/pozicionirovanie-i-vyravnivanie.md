# Позиционирование и выравнивание

## **Выравнивание**

### **Горизонтальное**

* **для любых элементов**

```css
.element {
    display: flex;
    justify-content: center;
}
```

* **элемент инлайновый?**

```css
.element {
    text-align: center;
}
```

* **элемент блочный?**

```css
.element {
    margin: 0 auto;
}
```

```text
      **○ высота известна?**
```

```css
.element {
    position: absolute; 
    left: 50%
    margin-left: отрицательный марджин, равный ширине центрируемого элемента / 2;
}
```

```text
      **○ высота неизвестна?**
```

```css
.element {
    position: absolute; 
    left: 50%
    transform: translateX(-50%);
}
```

### Вертикальное

* **для любых элементов**

```css
.element {
    display: flex;
    align-items: center;
}
```

* **элемент инлайновый?**

```css
.element {
    line-height: height родительского элемента;
}
```

* **элемент блочный?**

  ```text
      **○ высота известна?**
  ```

```css
.element {
    position: absolute; 
    top: 50%
    margin-top: отрицательный марджин, равный высоте центрируемого элемента / 2;
}
```

```text
      **○ высота неизвестна?**
```

```css
.element {
    position: absolute; 
    left: 50%
    transform: translateY(-50%);
}
```

\*\*\*\*

### Горизонтальное и вертикальное вместе

* высота и ширина известны?

```css
.element {
    position: absolute; 
    top: 50%
    left: 50%

    margin-top: отрицательный марджин, равный высоте центрируемого элемента / 2;
    margin-left: отрицательный марджин, равный ширине центрируемого элемента / 2;
}
```

* высота и ширина неизвестны?

```css
.element {
    position: absolute; 
    top: 50%
    left: 50%

    transform: translate(-50%);
}
```

* используйте flexbox

```css
.element {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

