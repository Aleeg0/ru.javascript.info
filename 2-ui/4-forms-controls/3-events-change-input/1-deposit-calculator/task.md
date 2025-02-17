важность: 5

---

# Депозитный калькулятор

Создайте интерфейс, позволяющий ввести сумму банковского вклада и процент, а затем рассчитать, какая это будет сумма через заданный промежуток времени.

Демо-версия:

[iframe src="solution" height="350" border="1"]

Любое изменение введённых данных должно быть обработано немедленно.

Формула:
```js
<<<<<<< HEAD
// initial: начальная сумма денег
// interest: проценты, например, 0.05 означает 5% в год
// years: сколько лет ждать
=======
// initial: the initial money sum
// interest: e.g. 0.05 means 5% per year
// years: how many years to wait
>>>>>>> 1dce5b72b16288dad31b7b3febed4f38b7a5cd8a
let result = Math.round(initial * (1 + interest) ** years);
```
