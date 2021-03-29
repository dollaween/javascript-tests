<div align="center">

# Тест по асинхронности

[Вопросы](https://github.com/dollaween/javascript-questions)
|
[Тесты](https://github.com/dollaween/javascript-tests)
|
[Задачи](https://github.com/dollaween/javascript-tasks)

</div>

---

##### 1. Какой будет порядок вывода консолей?

```javascript
(async () => { await console.log('Async Await') })()
setTimeout(() => console.log('Timeout'), 0)
Promise.resolve().then(() => console.log('Promise'))
console.log('Log')
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
const container = document.getElementById('container')
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

В тесте продемонстрирован side-эффект при исполнении микрозадач. В данном случае, пользовательское поведение будет исполнено иначе, чем прямой вызов функции.

Разберем работу движка по шагам:
1. Выполняется `button.click()`. Мы кладем его в стек вызовов.
2. Переходим в `handleClick` `button`-а.
3. Выполняем `Promise.resolve`. Он добавляет нам микротаску `then` в очередь. `Promise.resolve` исполняется.
4. Далее переходим в `console.log` и выводим `Moskow`.
5. Мы закончили тело `handleClick` `button`-а и выходим из него, снимаем его со стека. Но наш синхронный код (click) не закончился, потому что есть другие хендлеры и стек не очищен.
6. Переходим в `handleClick` `container`-а и выводим в `console.log` `Novosibirsk`.
7. Стек очистился, исполняется микротаска `then` и в `console.log` выводится `Piter`.

</p>
</details>

---

##### 3. Какой будет вывод?

```javascript
async function fn() {

  let result = await Promise
    .resolve(10)
    .then(x => x + 1)
    .catch(x => x + 2)
    .then(x => x + 3)

  console.log(result)
}

fn()
```

1. `11`
2. `12`
3. `13`
4. `14`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

</p>
</details>

---

##### 4. Какой будет вывод?

```javascript
const arr = [10, 100, 650, 25, 5, 50]

arr.forEach((item) => {
  setTimeout(() => console.log(item), item)
})
```

1. `10, 100, 650, 25, 5, 50`
2. `5, 10, 25, 50, 100, 650`
3. `50, 50, 50, 50, 50, 50`
4. `650, 100, 50, 25, 10, 5`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

В каждой итерации мы запускаем таймер, который запустит консоль через 10, 100, 650, 25, 5 и 50 мс.
</p>
</details>

---
