<div align="center">

<h1>Javascript. Тест по типам</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

</div>

---

<div align="center">

### Сравнение типов

</div>

---

##### 1. Какой будет вывод?

```javascript
console.log(NaN === NaN)
console.log(NaN == NaN)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
console.log([] === [])
console.log([] == [])
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
console.log({} === {})
console.log({} == {})
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
console.log('05' === 5)
console.log('05' == 5)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

При сравнении значений разных типов через оператор `==`, оба значения будут приведены к числу.

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
console.log(true == 1)
console.log(false == 0)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

При сравнении значений разных типов через оператор `==`, оба значения будут приведены к числу.

</p>
</details>

---

##### 6. Какой будет вывод?

```javascript
console.log([] == 1)
console.log([] == 0)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
console.log({} == 1)
console.log({} == 0)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

</p>
</details>


---

##### 8. Какой будет вывод?

```javascript
console.log('0' == 0)
console.log(Boolean('0') == Boolean(0))
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

`Boolean(0)` — `false`, `Boolean('0')` — `true`.

</p>
</details>

---

<div align="center">

### Другое

</div>

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
