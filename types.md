<div align="center">

# Тест по типам

[Вопросы](https://github.com/dollaween/javascript-questions)
|
[Тесты](https://github.com/dollaween/javascript-tests)
|
[Задачи](https://github.com/dollaween/javascript-tasks)

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

`NaN` возвращает `false` при любых сравнениях.

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

##### 9. Какой будет вывод?

```javascript
console.log('' == false)
console.log('0' == false)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

</p>
</details>

---

##### 10. Какой будет вывод?

```javascript
console.log(null === null)
console.log(null == null)
console.log(undefined === undefined)
console.log(undefined == undefined)
```

1. `true`, `true`, `true`, `true`
2. `false`, `false`, `false`, `false`
3. `true`, `false`, `true`, `false`
4. `false`, `true`, `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

</p>
</details>

---

##### 11. Какой будет вывод?

```javascript
console.log(null === undefined)
console.log(null == undefined)
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

##### 12. Какой будет вывод?

```javascript
console.log(null == 0)
console.log(undefined == 0)
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

##### 13. Какой будет вывод?

```javascript
console.log(null == 0)
console.log(undefined == 0)
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

##### 14. Какой будет вывод?

```javascript
console.log(null > null)
console.log(null >= null)
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

##### 15. Какой будет вывод?

```javascript
console.log(undefined > undefined)
console.log(undefined >= undefined)
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

##### 16. Какой будет вывод?

```javascript
console.log(null > 0)
console.log(null >= 0)
console.log(null == 0)
```

1. `true`, `true`, `true`
2. `false`, `false`, `false`
3. `false`, `true`, `true`
4. `false`, `true`, `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

</p>
</details>

---

##### 17. Какой будет вывод?

```javascript
console.log(2 > 1 > 2 === false)
```

1. `true`
2. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

</p>
</details>


---

##### 18. Какой будет вывод?

```javascript
console.log([1] > null)
```

1. `true`
2. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

```js
[1] > null
'1' > 0
1 > 0
true
```

</p>
</details>

---

##### 19. Какой будет вывод?

```javascript
console.log('true' == true)
console.log('false' == false)
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Оператор `==` вызывает преобразование в число.

```js
`true` == true
NaN == 1
false
```

```js
`false` == false
NaN == 0
false
```

</p>
</details>

---

##### 20. Какой будет вывод?

```javascript
console.log(null == '')
```

1. `true`
2. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Значение `null` равно только `null` или `undefined`.

</p>
</details>

---

##### 21. Какой будет вывод?

```javascript
console.log(!!true == !!false)
console.log(!!'true' == !!'false')
```

1. `true`, `true`
2. `false`, `false`
3. `true`, `false`
4. `false`, `true`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

```js
!!true == !!false
true == false
false
```

```js
!!'true' == !!'false'
true == true
true
```

</p>
</details>

---

##### 22. Какой будет вывод?

```javascript
console.log(['x'] == 'x')
```

1. `true`
2. `false`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

```js
['x'] == 'x'
'x' == 'x'
true
```

</p>
</details>

---

<div align="center">

### Вычисление

</div>

---

##### 1. Какой будет вывод?

```javascript
console.log('10' + 5)
console.log('10' - 5)
```

1. `15`, `5`
2. `105`, `105`
3. `105`, `15`
4. `15`, `105`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

```js
'10' + 5
'10' + '5'
'105'
```

```js
'10' - 5
10 - 5
5
```

</p>
</details>

---

##### 2. Какой будет вывод?

```javascript
console.log(1 + 2 + 'number')
console.log('number' + 1 + 2)
```

1. `12number`, `number12`
2. `3number`, `number3`
3. `3number`, `number12`
4. `12number`, `number3`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

```js
1 + 2 + 'number'
3 + 'number'
'3' + 'number'
'3number'
```

```js
'number' + 1 + 2
'number' + '1' + 2
'number1' + 2
'number1' + '2'
'number12'
```

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
console.log(null + undefined)
```

1. `null`
2. `undefined`
3. `object`
4. `NaN`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

```js
null + undefined
0 + NaN
NaN
```

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
console.log([1] + [1, 2])
```

1. `1,1,2`
2. `112`
3. `11,2`
4. `1,12`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

```js
[1] + [1, 2]
'1' + '1,2'
'11,2'
```

</p>
</details>

---

##### 5. Какой будет вывод?

```javascript
console.log('foo' + + 'bar')
```

1. `fooNaN`
2. `foonull`
3. `fooundefined`
4. `foobar`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Унарный оператор `+` имеет более высокий приоритет, чем обычный оператор `+`. В результате `+'bar'` вычисляется первым.

```js
'foo' + + 'bar'
'foo' + NaN
'fooNaN'
```

</p>
</details>

---

##### 6. Какой будет вывод?

```javascript
console.log([1, 2, 3] + [1, 2, 3])
```

1. `1,2,31,2,3`
2. `123123`
3. `66`
4. `6,6`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

```js
[1, 2, 3] + [1, 2, 3]
'1,2,3' + '1,2,3'
'1,2,31,2,3'
```

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
console.log({} + [] + {} + [1])
```

1. `0[object Object]1`
2. `0`
3. `1`
4. `4`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

```js
{} + [] + {} + [1]
+ [] + {} + [1]
0 + {} + [1]
0 + 'object Object' + [1]
'0[object Object]' + [1]
'0[object Object]' + '1'
'0[object Object]1'
```

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
console.log(! + [] + [] + ![])
```

1. `0`
2. `false`
3. `0false`
4. `truefalse`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

```js
! + [] + [] + ![]
(!+[]) + [] + (![])
!0 + [] + false
true + [] + false
true + '' + false
'truefalse'
```

</p>
</details>

---

<div align="center">

### Другое

</div>

---

##### 1. Какой будет вывод?

```javascript
console.log(typeof typeof NaN)
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
console.log(typeof null)
console.log(null instanceof Object)
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

##### 3. Какой будет вывод?

```javascript
console.log(typeof {} instanceof Object)
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

##### 4. Какой будет вывод?

```javascript
const hunter1 = { name: 'Sam' }
const hunter2 = { name: 'Din' }

console.log(hunter1 + hunter2)
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

##### 5. Какой будет вывод?

```javascript
const hunter1 = { name: 'Sam' }
const hunter2 = { name: 'Din' }

console.log(hunter1 >= hunter2)
console.log(hunter1 === hunter2)
console.log(hunter1 > hunter2)
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
