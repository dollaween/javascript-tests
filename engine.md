# Javascript. Тесты по движку

---

##### Какой будет вывод?
```javascript
console.log(user)
var user = 'Jon Snow'
```

1. `Jon Snow`
2. `null`
3. `undefined`
4. `ReferenceError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

</p>
</details>

---

##### Какой будет вывод?
```javascript
var person = 'Hodor';

function person() {
  return 'Hodor'
}

console.log(typeof person)
```

1. `Hodor`
2. `string`
3. `function`
4. `object`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

Во время создания контекста, функция объявляется и инициализируется сразу. Переменная же только объявляется, но не инициализируется.

Поэтому, когда дело доходит до строчки `var person = 'Hodor'`, то она перезатирает предыдущее значение `person`, т.е. в нашем случае функцию.

</p>
</details>

---

##### Какой будет вывод?

```javascript
console.log(city)
const city = 'Meereen'
```

1. `ReferenceError`
2. `SystemError`
3. `Meereen`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Во время создания контекста, переменные, объявленные через `const` и `let`, только объявляются, но не инициализируются.

</p>
</details>

---

##### Какой будет вывод?

```javascript
function outerFunction() {
  function innerFunction() {
    console.log(this)
  }
  innerFunction()
}
outerFunction()
```

1. `outerFunction`
2. `innerFunction`
3. `window`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

В контексте выполнения функции значение `this` зависит от того, как именно была вызвана функция. Если она вызвана в виде метода объекта, тогда значение `this` привязано к этому объекту. В других случаях `this` привязывается к глобальному объекту или устанавливается в `undefined` (в строгом режиме).

</p>
</details>

---


