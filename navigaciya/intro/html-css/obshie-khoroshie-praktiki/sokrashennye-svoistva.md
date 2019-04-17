# Сокращенные свойства

## • Background 

Многие разработчики зачастую ленятся писать развернутые свойства, и по итогу мы можем наблюдать в коде следующее:

```css
/* такаое */

.btn {
    background: #f0f0f0;
}

/* или такаое */

.btn {
    background: url('path/to/your/img');
}
```

#### Чем это может обернуться? 

Например, вы описали в классе first свойства фона в background, но специально не указали картинку. А потом классом second добавляете элементу картинку свойством background-image. И всё хорошо, картинка просто добавляется: first, second.

```css
.first {
  background: red no-repeat;
}
.second {
  background-image: url('picture.png');
}
```

Но если наоборот: сначала background-image, а потом остальное в сокращённом свойстве background, то картинки уже не будет — она затрётся.

```css
.second {
  background-image: url('picture.png');
}
.first {
  background: red no-repeat;
}
```

Поэтому, правильнее было бы написать код следующим образом:

```css
.first {
  background-color: red;
  background-repeat: no-repeat;
}
.second {
  background-image: url('picture.png');
}
```

