# Тестирование верстки на переполнение

## • **Избегайте фиксированной высоты**

### **Почему?**

При увеличении количества текста он вывалится наружу и может наложиться на соседние элементы.

### **Как это увидеть?**

Можно отредактировать исходный html, вставив больше текста, или же отредактировать DOM-элемент в панели разработчиков.

```markup
/* До */ 

<button class="btn">Отправить заявку</button>

/* После */ 

<button class="btn">Отправить заявкуОтправить заявкуОтправить заявкуОтправить заявкуОтправить заявку</button>
```

### **Как тогда сделать?**

Единого варианта решения нет. Все зависит от того, какого результата вам нужно достичь. Если у блока по макету есть минимальная высота, но недостаточно контента, чтобы этот блок растянуть, используйте **min-height**.

```css
/* Плохо */

.btn {
  height: 150px;
  padding: 10px;
}

/* Хорошо */

.btn {
  min-height: 150px;
  padding: 10px;
}
```

Если же контента достаточно, то **min-height** не нужен, достаточно задать стили для текста и **padding** для блока, и его размеры будут определяться содержимым. Также обратите внимание на то, есть ли у блока явные границы. Если они есть, при увеличении количества текста он может упереться в свои боковые края. В этом случае стоит добавить **padding** слева и справа, чтобы текст не прилипал к границам. Рассмотрим на примере кнопки:

![&#x41A;&#x43D;&#x43E;&#x43F;&#x43A;&#x430; &#x441; &#x437;&#x430;&#x434;&#x430;&#x43D;&#x43D;&#x43E;&#x439; &#x43C;&#x438;&#x43D;&#x438;&#x43C;&#x430;&#x43B;&#x44C;&#x43D;&#x43E;&#x439; &#x432;&#x44B;&#x441;&#x43E;&#x442;&#x43E;&#x439; &#x431;&#x435;&#x437; &#x43F;&#x430;&#x434;&#x434;&#x438;&#x43D;&#x433;&#x43E;&#x432;](https://github.com/2UP/methodology/tree/a276ea4d4c8276ef8834c525e77ea1dd71e3fc54/.gitbook/assets/image-3.png)

![&#x41F;&#x440;&#x438; &#x443;&#x432;&#x435;&#x43B;&#x438;&#x447;&#x435;&#x43D;&#x438;&#x438; &#x43A;&#x43E;&#x43B;&#x438;&#x447;&#x435;&#x441;&#x442;&#x432;&#x430; &#x442;&#x435;&#x43A;&#x441;&#x442;&#x430; &#x441;&#x43E;&#x434;&#x435;&#x440;&#x436;&#x438;&#x43C;&#x43E;&#x435; &#x43A;&#x43D;&#x43E;&#x43F;&#x43A;&#x438; &#x443;&#x43F;&#x438;&#x440;&#x430;&#x435;&#x442;&#x441;&#x44F; &#x432; &#x431;&#x43E;&#x43A;&#x43E;&#x432;&#x44B;&#x435; &#x43A;&#x440;&#x430;&#x44F;](https://github.com/2UP/methodology/tree/a276ea4d4c8276ef8834c525e77ea1dd71e3fc54/.gitbook/assets/image-2.png)

![&#x414;&#x43E;&#x431;&#x430;&#x432;&#x43B;&#x44F;&#x435;&#x43C; padding, &#x43A;&#x43D;&#x43E;&#x43F;&#x43A;&#x430; &#x431;&#x43E;&#x43B;&#x44C;&#x448;&#x435; &#x43D;&#x435; &#x43F;&#x440;&#x438;&#x43B;&#x438;&#x43F;&#x430;&#x435;&#x442; &#x43A; &#x43A;&#x440;&#x430;&#x44F;&#x43C;. &#x41C;&#x43E;&#x436;&#x43D;&#x43E; &#x441;&#x43F;&#x43E;&#x43A;&#x43E;&#x439;&#x43D;&#x43E; &#x434;&#x43E;&#x431;&#x430;&#x432;&#x438;&#x442;&#x44C; &#x435;&#x449;&#x435; &#x442;&#x435;&#x43A;&#x441;&#x442;&#x430;, &#x43A;&#x43D;&#x43E;&#x43F;&#x43A;&#x430; &#x43D;&#x435; &#x441;&#x43B;&#x43E;&#x43C;&#x430;&#x435;&#x442;&#x441;&#x44F;](https://github.com/2UP/methodology/tree/a276ea4d4c8276ef8834c525e77ea1dd71e3fc54/.gitbook/assets/image-4.png)

