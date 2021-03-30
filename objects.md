<div align="center">

# Тест по объектам

[Вопросы](https://github.com/dollaween/javascript-questions)
|
[Тесты](https://github.com/dollaween/javascript-tests)
|
[Задачи](https://github.com/dollaween/javascript-tasks)

</div>

---

##### 1. Какой будет вывод?

```javascript
const obj = {
  '2abc': '2abc',
  3: 3,
  '1': '1',
  1: 1,
  '-1': '-1',
  2: 2
}

console.log(Object.keys(obj))
```

1. ["1", "2", "3", "2abc", "-1"]
3. ["-1", "1", "2", "2abc", "3"]
4. ["1", "2", "2abc", "3", "-1"]
5. ["-1", "1", "2", "3", "2abc"]

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

Объект сортирует ключи следующим образом: сперва идут положительные целочисленные ключи, а затем все остальные ключи в порядке их записи.

Если у двух ключей совпадают имена, то останется последний из них.

</p>
</details>
