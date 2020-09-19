# Javascript Test: Async

---

##### 1. Какой будет порядок вывода консолей?

```javascript
(async () => { await console.log('Async Await'); })()
setTimeout(() => console.log('Timeout'), 0);
Promise.resolve().then(() => console.log('Promise'));
console.log('Log');
```

1. `Async Await`, `Timeout`, `Promise`, `Log`
2. `Log`, `Async Await`, `Promise`, `Timeout`
3. `Async Await`, `Log`, `Promise`, `Timeout`
4. `Log`, `Async Await`, `Timeout`, `Promise`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `3`

</p>
</details>

---

##### 2. Какой будет порядок вывода консолей?

```html
<div id="container">
  <div id="button">Get cities</div>
</div>
```

```javascript
const container = document.getElementById('container');
const button = document.getElementById('button')

button.addEventListener('click', () => {
  Promise.resolve()
    .then(() => console.log('Piter'))

  console.log('Moscow')
})

container.addEventListener('click', () => {
  console.log('Novosibirsk')
})

button.click()
```

1. `Moscow` `Piter` `Novosibirsk`
2. `Piter` `Moscow` `Novosibirsk`
3. `Novosibirsk` `Moscow` `Piter`
4. `Moscow` `Novosibirsk` `Piter`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

</p>
</details>
