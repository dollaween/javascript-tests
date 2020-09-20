<div align="center">

<h1>Javascript. Тест по типам</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

</div>

---

##### 1. Какой будет вывод?

```javascript
console.log( NaN === NaN )
```

1. `true`
2. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

</p>
</details>

---

##### 2. Какой будет вывод?

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

##### 3. Какой будет вывод?

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

##### 4. Какой будет вывод?

```javascript
console.log( typeof {} instanceof Object )
```

1. `boolean`
2. `object`
3. `true`
4. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

Сперва будет выполнен оператор `typeof {}`. Далее мы получим операцию:
```javascript
'object' instanceof Object
```

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
const hunter1 = { name: 'Sam' }
const hunter2 = { name: 'Din' }

console.log( hunter1 + hunter2 )
```

1. `[object Object][object Object]`
2. `{ name: 'Din' }`
3. `{ name: 'SamDin' }`
4. `SamDin`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

</p>
</details>

---

##### 6. Какой будет вывод?

```javascript
const hunter1 = { name: 'Sam' }
const hunter2 = { name: 'Din' }

console.log( hunter1 >= hunter2 )
console.log( hunter1 === hunter2 )
console.log( hunter1 > hunter2 )
```

1. `true` `false` `false`
2. `false` `false` `false`
3. `false` `true` `false`
4. `true` `true` `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

</p>
</details>
