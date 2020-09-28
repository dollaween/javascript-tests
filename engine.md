<div align="center">

<h1>Javascript. Тест по движку</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

</div>

---

##### 1. Какой будет вывод?
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

Во время создания лексического окружения переменным, объявленным через `var`, присваивается значение `undefined`.

</p>
</details>

---

##### 2. Какой будет вывод?
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

##### 3. Какой будет вывод?

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

##### 4. Какой будет вывод?

```javascript
function outer() {
  function inner() {
    console.log(this)
  }
  inner()
}
outer()
```

1. `outer`
2. `inner`
3. `window`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

В контексте выполнения функции значение `this` зависит от того, как именно была вызвана функция. Если она вызвана в виде метода объекта, тогда значение `this` привязано к этому объекту. В других случаях `this` привязывается к глобальному объекту или устанавливается в `undefined` (в строгом режиме).

В браузере глобальным объектом является `window`, в Node.js — `global`.

</p>
</details>

---

##### 5. В какую области видимости будет записана переменная `name`?

```javascript

function outer() {
  function inner() {
    name = 'Luke'
  }
  inner()
}
outer()

```

1. Глобальную
2. `outer`
3. `inner`
4. `SystemError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Когда встречается переменная без ключевого слова `var`, `const`, `let` — она записывается в глобальную область видимости. В браузере это объект `window`, в Node.js — объект `global`.

В строгом моде `use strict` будет выброшена ошибка `ReferenceError`.

</p>
</details>

---

##### 6. Какой будет вывод?

```javascript
const user = {
  login: 'Darth Vader',
  sayHello: () => {
    return `Hello, i'm ${this.login}`
  }
}

console.log(user.sayHello());
```

1. `Hello, i'm Darth Vader`
2. `Hello, i'm`
3. `Hello, u'm null`
4. `Hello, i'm undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 4**

У стрелочных функций нет `this`. Если происходит обращение к `this`, его значение берется снаружи. 

В данном случае, `this` будет указывать на глобальный объект, у которого нет свойства `login`.

</p>
</details>

---

##### 7. Какой будет вывод?

```javascript
function iKnowYourName() {
  function getName() {
    return arguments[0]
  }

  const getLastname = () => {
    return arguments[1]
  }

  return `Your name is: ${getName()} ${getLastname()}`
}

console.log( iKnowYourName('Darth', 'Vader') )
```

1. `Your name is Darth Vader`
2. `Your name is undefined Vader`
3. `Your name is Darth undefined`
4. `Your name is undefined undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

У стрелочных функций отсутствует переменная `arguments`.

В данном случае функция `getName` обращается к своей переменной `arguments`, а функция `getLastName` берет `arguments` из функции `iKnowYourName`.

</p>
</details>

---

##### 8. Какой будет вывод?

```javascript
const fighter = {
  name: 'Cassie',
  sayName: function() {
    console.log(this.name)
  }
}

const fn = fighter.sayName.bind(fighter).bind({ name: 'Sonya' })
fn()
```

1. `Cassie`
2. `Sonya`
3. `undefined`
4. `SystemError`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Метод `bind` привязывает контекст навсегда. Повторный вызов `bind` будет игнорироваться.

</p>
</details>

---

##### 9. Какой будет вывод?

```javascript
let winner = 'Sub-Zero'

function getWinner() {
  let winner = 'Scorpion'

  let result = function() {
    console.log(winner)
  }

  result.winner = 'Jax'

  return result
}

getWinner().bind({ winner: 'Johny' })()
```

1. `Sub-Zero`
2. `Scorpion`
3. `Jax`
4. `Johny`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 2**

`this` у стрелочных функций берется из внешнего контекста, в данном случае — из функции `getWinner`.

</p>
</details>

---

##### 10. Какой будет порядок alert'ов?

```html
<div id="container">
  <div id="video">
    <button id="button">Play!</button>
  </div>
</div>
```

```javascript
button.addEventListener('click', () => alert('button'), false)
video.addEventListener('click', () => alert('video'), false)
container.addEventListener('click', () => alert('container'), true)
```

1. `container` `video` `button`
2. `button` `video` `container`
3. `container` `button` `video`
4. `button` `container` `video`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 3**

Третьим аргументом в `addEventListener` устанавливается захват (`capture`), который определяет на какой стадии будет исполнен обработчик: `true` — на стадии захвата, `false` – на стадии всплытия.

В первую очередь будут выполнены все слушатели со значением `true` в порядке вложенности от предка к потомку. Затем будут выполнены все слушатели со значением `false` в обратном порядке.

</p>
</details>

---

##### 11. Какой будет вывод?

```html
<div id="container">
  <button id="button">Play!</button>
</div>
```

```javascript
button.addEventListener('click', () => {});
container.addEventListener('click', fn);

function fn(e) {
  console.log(e.target.tagName, e.currentTarget.tagName, this.tagName);
}
```

1. `BUTTON` `DIV` `DIV`
2. `DIV` `DIV` `DIV`
3. `BUTTON` `BUTTON` `BUTTON`
4. `BUTTON` `BUTTON` `DIV`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

`e.target` — это исходный элемент, на котором произошло событие, в процессе всплытия он неизменен.

`e.currentTarget` — это текущий элемент, до которого дошло всплытие.

Если функция была определена не как стрелочная, то `e.currentTarget` и `this` совпадают.

</p>
</details>

---
