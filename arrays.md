<div align="center">

# Тест по массивам

[Вопросы](https://github.com/dollaween/javascript-questions)
|
[Тесты](https://github.com/dollaween/javascript-tests)
|
[Задачи](https://github.com/dollaween/javascript-tasks)

</div>

---

##### 1. Какой будет вывод?

```javascript
let numbers = [1, 2, 3]
numbers.filter((item) => item > 1)

console.log(numbers)
```

1. `[1, 2, 3]`
2. `[2, 3]`
3. `[1]`
4. `undefined`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ:** `1`

Метод `filter()` создает новый массив со всеми элементами, прошедшими проверку, но не изменяет исходный массив. Поэтому массив `numbers` такой же, каким был изначально.

</p>
</details>
