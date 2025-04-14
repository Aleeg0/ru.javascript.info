
<<<<<<< HEAD
Открывающий тег -- это `pattern:\[(b|url|quote)]`.
=======
Opening tag is `pattern:\[(b|url|quote)]`.
>>>>>>> 540d753e90789205fc6e75c502f68382c87dea9b

Затем, чтобы найти всё до закрывающего тега -- используем выражение `pattern:.*?` с флагом `pattern:s`: оно найдёт любые символы, включая новую строку, и затем добавим обратную ссылку на открывающий тег.

<<<<<<< HEAD
Полное выражение: `pattern:\[(b|url|quote)\].*?\[/\1]`.
=======
The full pattern: `pattern:\[(b|url|quote)\].*?\[/\1]`.
>>>>>>> 540d753e90789205fc6e75c502f68382c87dea9b

В действии:

```js run
let regexp = /\[(b|url|quote)].*?\[\/\1]/gs;

let str = `
  [b]привет![/b]
  [quote]
    [url]http://ya.ru[/url]
  [/quote]
`;

alert( str.match(regexp) ); // [b]привет![/b],[quote][url]http://ya.ru[/url][/quote]
```

<<<<<<< HEAD
Обратите внимание, что кроме экранирования `pattern:[` нам необходимо экранировать слеш в закрывающем теге `pattern:[\/\1]`, потому что обычно слеш завершает паттерн.
=======
Please note that besides escaping `pattern:[`, we had to escape a slash for the closing tag `pattern:[\/\1]`, because normally the slash closes the pattern.
>>>>>>> 540d753e90789205fc6e75c502f68382c87dea9b
