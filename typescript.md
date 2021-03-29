<div align="center">

# Тест по Typescript

[Вопросы](https://github.com/dollaween/javascript-questions)
|
[Тесты](https://github.com/dollaween/javascript-tests)
|
[Задачи](https://github.com/dollaween/javascript-tasks)

</div>

---

##### Какой будет вывод?

```typescript
const fruits: [string, string] = ['apple', 'orange']
fruits.push('banana')

console.log(fruits);
```

1. `["apple", "orange", "banana"]`
2. `["apple", "orange"]`
3. `Tuple type '[string, string]' of length '2' has no element at index '2'`
4. `Type 'string' is not assignable to type 'undefined'`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Тип `Tuple` может быть расширен путем использования метода `push`.

Чтобы запретить подобное, нужно добавить параметр `readonly`:
```typescript
const fruits: readonly [string, string] = ['apple', 'orange']
```

</p>
</details>
