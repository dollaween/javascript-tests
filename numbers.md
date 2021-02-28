<div align="center">

<h1>Javascript. Тесты по числам</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

</div>

---

##### 1. Какой будет вывод?

```javascript
let num = 2**53
// 9007199254740992

console.log(num + 5)
```

1. `9007199254740997`
2. `9007199254740996`
3. `Error: Too Big Number`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Из-за ограничений в вычислениях, `2**53` — это максимальное число, которое обеспечивает точность вычислений. Оно же хранится в константе Number.MAX_SAFE_INTEGER.

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
console.log(Infinity - Infinity)
```

1. `Infinity`
2. `-Infinity`
3. `NaN`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
console.log(-1 / 0)
```

1. `Infinity`
2. `-Infinity`
3. `NaN`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
console.log(-Infinity + NaN)
```

1. `Infinity`
2. `-Infinity`
3. `NaN`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
console.log(Number.isInteger(0))
console.log(Number.isInteger('0'))
console.log(Number.isInteger(1.0))
console.log(Number.isInteger(1.0000000000000001))
```

1. `false false true false`
2. `true false true false`
3. `true true true false`
4. `true false true true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Метод `Number.isInteger()` — определяет, является ли переданное значение целым числом.

Из-за неточности в вычислениях, мы имеем следующее:
* `Number.isInteger(1.000000000000001)` — `false`
* `Number.isInteger(1.0000000000000001)` — `true`
* `Number.isInteger(1.00000000000000001)` — `true`

</p>
</details>


---

##### 6. Какой будет вывод?

```javascript
const n = 10
const answer = n++ + n++
console.log()
```

1. `20`
2. `21`
3. `22`
4. `23`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

</p>
</details>
