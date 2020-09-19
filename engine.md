# Javascript. Тесты по движку

---

##### Какой будет вывод?
```
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
