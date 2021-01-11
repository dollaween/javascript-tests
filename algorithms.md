<div align="center">

<h1>Javascript. Тест по массивам</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

</div>

---

##### 1. Какой пример отбрасывания неважной сложности неверен?

```javascript
1. O(N^2 + N) = O(N^2)
2. O(N + log N) = O(N)
3. O(5 * 2^N + 10 * N^100) = O(N^100)
4. O(N^2 + B) = O(N^2 + B)
```

1. `1`
2. `2`
3. `3`
4. `4`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `3`

Правильный вариант будет: `O(5 * 2^N + 10 * N^100) = O(2^N)`. Здесь `5` и `10` являются константами, поэтому от них мы избавляемся. Степенная функция растет гораздо быстрее, поэтому остается `2^N`.

В примере `O(N + log N)`, `log N` намного меньше чем `N`.

В примере `O(N^2 + B)` ничего не может быть упрощено, потому что мы ничего не знаем о `B`.

</p>
</details>

---

##### 2. Чему будет равна нотация О большое?

```javascript
function sum(n) {
  if (n === 1) return 1
  return n + sum(n - 1)
}
```

1. `O(1)`
2. `O(N)`
3. `O(N^2)`
4. `O(log N)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `2`

Быстродействие этой функции прямо пропорционально входному значению аргумента `n`:
* если `n === 3`, то функция вызывает сама себя 3 раза
* если `n === 100`, то функция вызовет сама себя 100 раз

</p>
</details>

---

##### 3. Чему будет равна нотация О большое для функции `pairSum`?

```javascript
function pairSum(n) {
  let sum = 0
  for (let i = 0; i < n; i++) {
    sum += sum(i, i + 1)
  }
}

function sum(a, b) {
  return a + b
}
```

1. `O(1)`
2. `O(N)`
3. `O(N^2)`
4. `O(log N)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `2`

Сложность функции `sum` равна `O(1)`, так как она всегда выполняет константное количество операций.

Функция `pairSum` в цикле складывает некоторые пары чисел. Ее сложность прямо пропорциональна входному аргументу `n`, так как чем больше `n`, тем больше раз будет выполнен цикл.

</p>
</details>

---

##### 4. Чему будет равна нотация О большое для обоих функций?

```javascript
function first(n) {
  let min = Number.MIN_VALUE
  let max = Number.MAX_VALUE
  for (let i = 0; i < n; i++) {
    if (i < min) min = i
    if (i > max) min = i
  }
  return [min, max]
}

function second(n) {
  let min = Number.MIN_VALUE
  let max = Number.MAX_VALUE
  for (let i = 0; i < n; i++) {
    if (i < min) min = i
  }
  for (let i = 0; i < n; i++) {
    if (i > max) max = i
  }
  return [min, max]
}
```

1. `O(1)`, `O(1)`
2. `O(1)`, `O(N)`
3. `O(N)`, `O(N)`
4. `O(N)`, `O(N^2)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `3`

Big O показывает как ведут себя алгоритмы. Хоть функция `first` и будет выполняться быстрее функции `second`, оба алгоритма имеют сложность `O(N)`.

</p>
</details>

---

##### 5. Чему равна нотация О большое?

```javascript
function print(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let k = 0; k < arr.length; k++) {
      console.log(arr[i], arr[k])
    }
  }
}
```

1. `O(1)`
2. `O(N)`
3. `O(N^2)`
4. `O(log N)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `3`

Приведем цикл к псевдокоду:
```javascript
function print(arr) {
  for ()    // N раз
    for ()  // N раз
}
```

Так как циклы зависимы друг от друга, то мы перемножаем сложности `N * N` и получаем `N^2`.

</p>
</details>

---

##### 6. Чему равна нотация О большое?

```javascript
function print(arr) {
  for (let i = 0; i < arr.length; i++) {
    for (let k = i; k < arr.length; k++) {
      console.log(arr[i], arr[k])
    }
  }
}
```

1. `O(1)`
2. `O(N)`
3. `O(N^2)`
4. `O(log N)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `3`

Приведем цикл к псевдокоду:
```javascript
function print(arr) {
  for ()    // N раз
    for ()  // N, N - 1, N - 2, ..., 1 раз
}
```

Итого мы получаем такую сложность: `O(N + (N - 1) + (N - 2) + ... + 1)`.

Сложность цикла можно упростить до `N^2 / 2` или, после отбрасывания констант, до `N^2`.

</p>
</details>

---

##### 7. Чему равна нотация О большое?

```javascript
function print(arrA, arrB) {
  for (let i = 0; i < arrA.length; i++) {
    for (let k = 0; k < arrB.length; k++) {
      console.log(arrA[i], arrB[k])
    }
  }
}
```

1. `O(N)`
2. `O(N^2)`
3. `O(A + B)`
4. `O(A * B)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `4`

Приведем цикл к псевдокоду:
```javascript
function print(arr) {
  for ()    // A раз
    for ()  // B раз
}
```

Так как циклы зависимы друг от друга, то мы перемножаем сложности и получаем `A * B`.

</p>
</details>

---

##### 8. Чему равна нотация О большое?

```javascript
function print(arrA, arrB) {
  for (let i = 0; i < arrA.length; i++) {
    for (let k = 0; k < arrB.length; k++) {
      for (let t = 0; t < 100000; t++) {
        console.log(arrA[i], arrB[k])
      }
    }
  }
}
```

1. `O(N^2)`
2. `O(A + B)`
3. `O(A * B)`
4. `O(A * B * t)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `3`

Приведем цикл к псевдокоду:
```javascript
function print(arr) {
  for ()        // A раз
    for ()      // B раз
      for ()    // константное число раз
}
```

`100000` — это константа, а при учете сложности мы не учитываем константы. Поэтому все будет точно так же, как в предыдущей задаче.

</p>
</details>

---

##### 9. Чему равна нотация О большое?

```javascript
function print(arr) {
  for (let i = 0; i < arr.length / 2; i++) {
    console.log(arr[i])
  }
}
```

1. `O(1)`
2. `O(N)`
3. `O(N^2)`
4. `O(log N)`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `2`

Приведем функцию к псевдокоду:
```javascript
function print(arr) {
  for ()        // N / 2 раз
}
```

Здесь мы идем до половины массива, значит сложность будет `O(N / 2) = O(N)`.

Почему не `log N`? Потому что мы берем половину массива в общем, а не в каждой итерации.

</p>
</details>
