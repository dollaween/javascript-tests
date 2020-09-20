<div align="center">

<h1>Javascript. Тесты по числам</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

</div>

---

##### 1. Какой будет вывод?

```javascript
let bigNumber = 2**53
// 9007199254740992

console.log(bigNumber + 5)
```

1. `9007199254740997`
2. `9007199254740996`
3. `Error: Too Big Number`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Из-за ограничений в вычислениях, `2**53` — это максимальное число, которое обеспечивает точность вычислений.

</p>
</details>
