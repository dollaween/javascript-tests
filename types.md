<div align="center">

<h1>Javascript. Тест по типам</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

</div>

---

##### 1. Какой будет вывод?

```javascript
console.log( typeof typeof NaN )
```

1. `number`
2. `string`
3. `NaN`
4. `SyntaxError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Операцию можно разложить на две:
```javascript
typeof NaN
// 'number'

typeof 'number'
// string
```

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
console.log( typeof null )
console.log( null instanceof Object )
```

1. `null` `true`
2. `null` `false`
3. `object` `true`
4. `object` `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

</p>
</details>

---
