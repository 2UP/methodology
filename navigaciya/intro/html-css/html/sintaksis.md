# Синтаксис HTML

* Для отступов у вложенных элементов используется tab. Для правильного форматирования используйте файл [.editorconfig](https://github.com/htmlacademy/codeguide/blob/master/.editorconfig) в вашем редакторе.
* Теги и их атрибуты пишутся строчными буквами. Для значений атрибутов всегда используются двойные кавычки.
* Необязательный закрывающий слеш у одиночных тегов \(`<img>`, `<br>` и другие\) не ставится.
* Необязательные закрывающие теги \(например, `</li>` или `</body>`\) не пропускаются.
* Для проверки HTML-кода используйте файл конфигурации [.htmlhintrc](https://github.com/htmlacademy/codeguide/blob/master/.htmlhintrc) для настройки валидатора [HTMLHint](http://htmlhint.com/).

```markup
<!DOCTYPE html>
<html lang="ru">
  <head>
    <meta charset="utf-8">
    <title>Страница о коте</title>
  </head>
  <body>
    <article class="post">
      <h1>Красивый кот</h1>
      <figure class="post-item">
        <img src="cat.jpg" alt="Изображение кота">
        <figcaption>Кот красив!</figcaption>
      </figure>
    </article>
  </body>
</html>
```



