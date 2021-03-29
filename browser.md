<div align="center">

# Тест по браузерному API

[Вопросы](https://github.com/dollaween/javascript-questions)
|
[Тесты](https://github.com/dollaween/javascript-tests)
|
[Задачи](https://github.com/dollaween/javascript-tasks)

</div>

---

##### 1. Какой будет вывод?

```javascript
const user = {
  login: 'Adler',
  password: 'SHER'
}

localStorage.setItem('user', user)
sessionStorage.setItem('user', user)

console.log( localStorage.getItem('user') )
console.log( sessionStorage.getItem('user') )
```

1. `[object Object]` `[object Object]`
2. `[object Object]` `{ login: 'Adler', password: 'SHER' }`
3. `{ login: 'Adler', password: 'SHER' }` `[object Object]`
4. `null` `null`

<details><summary><b>Ответ</b></summary>
<p>

**Ответ: 1**

`localStorage` и `sessionStorage` хранят данные только в виде строк. Когда нам приходит объект, он преобразуется в строку `[object Object]`.

`localStorage` и `sessionStorage` имеют одно и то же API и ведут себя идентично, за исключением некоторых условий:
1. `localStorage` один на всех вкладках в рамках одного истоничка, `sessionStorage` на каждой вкладке свой.
2. `localStorage` сохраняется после перезапуска браузера и ОС, `sessionStorage` пропадает даже после закрытия/открытия вкладки.

</p>
</details>

