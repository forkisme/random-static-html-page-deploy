EN

-   <a href="https://ar.javascript.info/" class="supported-langs__link"><span class="supported-langs__brief">AR</span><span class="supported-langs__title">عربي</span></a>
-   <a href="https://javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">EN</span><span class="supported-langs__title">English</span></a>
-   <a href="https://es.javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">ES</span><span class="supported-langs__title">Español</span></a>
-   <a href="https://fr.javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">FR</span><span class="supported-langs__title">Français</span></a>
-   <a href="https://id.javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">ID</span><span class="supported-langs__title">Indonesia</span></a>
-   <a href="https://it.javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">IT</span><span class="supported-langs__title">Italiano</span></a>

<!-- -->

-   <a href="https://ja.javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">JA</span><span class="supported-langs__title">日本語</span></a>
-   <a href="https://ko.javascript.info/" class="supported-langs__link"><span class="supported-langs__brief">KO</span><span class="supported-langs__title">한국어</span></a>
-   <a href="https://learn.javascript.ru/task/delay" class="supported-langs__link"><span class="supported-langs__brief">RU</span><span class="supported-langs__title">Русский</span></a>
-   <a href="https://tr.javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">TR</span><span class="supported-langs__title">Türkçe</span></a>
-   <a href="https://zh.javascript.info/task/delay" class="supported-langs__link"><span class="supported-langs__brief">ZH</span><span class="supported-langs__title">简体中文</span></a>

We want to make this open-source project available for people all around the world.

[Help to translate](https://javascript.info/translate) the content of this tutorial to your language!

<a href="/" class="sitetoolbar__link sitetoolbar__link_logo"><img src="/img/sitetoolbar__logo_en.svg" class="sitetoolbar__logo sitetoolbar__logo_normal" role="presentation" width="200" /><img src="/img/sitetoolbar__logo_small_en.svg" class="sitetoolbar__logo sitetoolbar__logo_small" role="presentation" width="70" /></a>

<a href="/ebook" class="buy-book-button"><span class="buy-book-button__extra-text">Buy</span>EPUB/PDF</a>

Search

Search

<a href="/tutorial/map" class="map"><span class="map__text">Tutorial map</span></a>

<span class="share-icons__title">Share</span><a href="https://twitter.com/share?url=https%3A%2F%2Fjavascript.info%2Ftask%2Fdelay" class="share share_tw"></a><a href="https://www.facebook.com/sharer/sharer.php?s=100&amp;p%5Burl%5D=https%3A%2F%2Fjavascript.info%2Ftask%2Fdelay" class="share share_fb"></a>

عربيEnglishEspañolFrançaisIndonesiaItaliano日本語한국어РусскийTürkçe简体中文

<a href="/" class="breadcrumbs__link"><span class="breadcrumbs__hidden-text">Tutorial</span></a>

<a href="/js" class="breadcrumbs__link"><span>The JavaScript language</span></a>

<a href="/advanced-functions" class="breadcrumbs__link"><span>Advanced working with functions</span></a>

<a href="/call-apply-decorators" class="breadcrumbs__link"><span>Decorators and forwarding, call/apply</span></a>

<a href="/call-apply-decorators" class="task-single__back"><span>back to the lesson</span></a>

## Delaying decorator

<span class="task__importance" title="How important is the task, from 1 to 5">importance: 5</span>

Create a decorator `delay(f, ms)` that delays each call of `f` by `ms` milliseconds.

For instance:

    function f(x) {
      alert(x);
    }

    // create wrappers
    let f1000 = delay(f, 1000);
    let f1500 = delay(f, 1500);

    f1000("test"); // shows "test" after 1000ms
    f1500("test"); // shows "test" after 1500ms

In other words, `delay(f, ms)` returns a "delayed by `ms`" variant of `f`.

In the code above, `f` is a function of a single argument, but your solution should pass all arguments and the context `this`.

[Open a sandbox with tests.](https://plnkr.co/edit/S979fqC4ga95OKUV?p=preview)

solution

The solution:

<a href="#" class="toolbar__button toolbar__button_run" title="run"></a>

<a href="#" class="toolbar__button toolbar__button_edit" title="open in sandbox"></a>

    function delay(f, ms) {

      return function() {
        setTimeout(() => f.apply(this, arguments), ms);
      };

    }

    let f1000 = delay(alert, 1000);

    f1000("test"); // shows "test" after 1000ms

Please note how an arrow function is used here. As we know, arrow functions do not have own `this` and `arguments`, so `f.apply(this, arguments)` takes `this` and `arguments` from the wrapper.

If we pass a regular function, `setTimeout` would call it without arguments and `this=window` (assuming we’re in the browser).

We still can pass the right `this` by using an intermediate variable, but that’s a little bit more cumbersome:

    function delay(f, ms) {

      return function(...args) {
        let savedThis = this; // store this into an intermediate variable
        setTimeout(function() {
          f.apply(savedThis, args); // use it here
        }, ms);
      };

    }

[Open the solution with tests in a sandbox.](https://plnkr.co/edit/sE5fOcbTxHuLo1fm?p=preview)

-   © 2007—2021  Ilya Kantor
-   <a href="/about" class="page-footer__link">about the project</a>
-   <a href="/about#contact-us" class="page-footer__link">contact us</a>
-   <a href="/terms" class="page-footer__link">terms of usage</a>
-   <a href="/privacy" class="page-footer__link">privacy policy</a>