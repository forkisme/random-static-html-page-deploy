EN

-   <a href="https://ar.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">AR</span><span class="supported-langs__title">عربي</span></a>
-   <a href="https://javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">EN</span><span class="supported-langs__title">English</span></a>
-   <a href="https://es.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">ES</span><span class="supported-langs__title">Español</span></a>
-   <a href="https://fr.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">FR</span><span class="supported-langs__title">Français</span></a>
-   <a href="https://id.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">ID</span><span class="supported-langs__title">Indonesia</span></a>
-   <a href="https://it.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">IT</span><span class="supported-langs__title">Italiano</span></a>

<!-- -->

-   <a href="https://ja.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">JA</span><span class="supported-langs__title">日本語</span></a>
-   <a href="https://ko.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">KO</span><span class="supported-langs__title">한국어</span></a>
-   <a href="https://learn.javascript.ru/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">RU</span><span class="supported-langs__title">Русский</span></a>
-   <a href="https://tr.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">TR</span><span class="supported-langs__title">Türkçe</span></a>
-   <a href="https://zh.javascript.info/task/increment-order" class="supported-langs__link"><span class="supported-langs__brief">ZH</span><span class="supported-langs__title">简体中文</span></a>

We want to make this open-source project available for people all around the world.

[Help to translate](https://javascript.info/translate) the content of this tutorial to your language!

<a href="/" class="sitetoolbar__link sitetoolbar__link_logo"><img src="/img/sitetoolbar__logo_en.svg" class="sitetoolbar__logo sitetoolbar__logo_normal" role="presentation" width="200" /><img src="/img/sitetoolbar__logo_small_en.svg" class="sitetoolbar__logo sitetoolbar__logo_small" role="presentation" width="70" /></a>

<a href="/ebook" class="buy-book-button"><span class="buy-book-button__extra-text">Buy</span>EPUB/PDF</a>

Search

Search

<a href="/tutorial/map" class="map"><span class="map__text">Tutorial map</span></a>

<span class="share-icons__title">Share</span><a href="https://twitter.com/share?url=https%3A%2F%2Fjavascript.info%2Ftask%2Fincrement-order" class="share share_tw"></a><a href="https://www.facebook.com/sharer/sharer.php?s=100&amp;p%5Burl%5D=https%3A%2F%2Fjavascript.info%2Ftask%2Fincrement-order" class="share share_fb"></a>

عربيEnglishEspañolFrançaisIndonesiaItaliano日本語한국어РусскийTürkçe简体中文

<a href="/" class="breadcrumbs__link"><span class="breadcrumbs__hidden-text">Tutorial</span></a>

<a href="/js" class="breadcrumbs__link"><span>The JavaScript language</span></a>

<a href="/first-steps" class="breadcrumbs__link"><span>JavaScript Fundamentals</span></a>

<a href="/operators" class="breadcrumbs__link"><span>Basic operators, maths</span></a>

<a href="/operators" class="task-single__back"><span>back to the lesson</span></a>

## The postfix and prefix forms

<span class="task__importance" title="How important is the task, from 1 to 5">importance: 5</span>

What are the final values of all variables `a`, `b`, `c` and `d` after the code below?

    let a = 1, b = 1;

    let c = ++a; // ?
    let d = b++; // ?

solution

The answer is:

-   `a = 2`
-   `b = 2`
-   `c = 2`
-   `d = 1`

<a href="#" class="toolbar__button toolbar__button_run" title="run"></a>

<a href="#" class="toolbar__button toolbar__button_edit" title="open in sandbox"></a>

    let a = 1, b = 1;

    alert( ++a ); // 2, prefix form returns the new value
    alert( b++ ); // 1, postfix form returns the old value

    alert( a ); // 2, incremented once
    alert( b ); // 2, incremented once

-   © 2007—2021  Ilya Kantor
-   <a href="/about" class="page-footer__link">about the project</a>
-   <a href="/about#contact-us" class="page-footer__link">contact us</a>
-   <a href="/terms" class="page-footer__link">terms of usage</a>
-   <a href="/privacy" class="page-footer__link">privacy policy</a>