
**Скрипт ротации номера телефона на странице**

[![Watch the video](https://github.com/profidela/elementary/blob/rotate/app/assets/img/preview.jpg)](https://youtu.be/11nF4psW77g)
![Alt text](app/assets/img/preview.jpg?raw=true "Title")

Поддержка использования как на .php страницах, так и .html c использованием javascript.

## Как использовать?

__1. C помощью файлового менеджера загрузить папку app в папку сайта__

__2. Вставить код на странице__

*PHP (Если фаил с расширением .php)*
```

<?php 
    //Разместить в самом начале страницы
    require('app/app.php'); 
?>
```
```
//[1] На странице ратируется номер телефона, одинаковых номеров может быть несколько на странице.
<?=$phone?>


//[2] А так же номера могут ратироваться и быть разными на странице.
<?=$phone[1]?>
<?=$phone[2]?>
<?=$phone[3]?>

//[3] Вывод номера может меняться только поcле клика на cсылку где N это номер потока,

<a href="#" <?=$_link[N]?>>[Нажми]</a> 
<?=$_phone[N]?>

... количество потоков возможно от 0 .. 99

```

__3. Редактировать фаил настроек app/app.ini и пароля входа в админку, хэш пароля можно сгенерировать здесь http://www.md5.cz/__

__4. Перейти в админ-панель авторизоваться  [http://ваша_веб_страница/?m=admin](http://ваш-сайт/ваша-страница/?m=admin)__

*Логин:* ``` demo2@demo.com ```
*Пароль:* ``` demo ```