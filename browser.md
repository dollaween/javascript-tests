<div align="center">

<h1>Javascript. Тест по движку</h1>

<a href="https://github.com/dollaween/javascript-tests">На главную</a> | <a href="https://github.com/dollaween/javascript-questions">Вопросы</a> | <a href="https://github.com/dollaween/javascript-tasks">Задачи</a>

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

`localStorage` и `sessionStorage` имеют одно и то же API и ведут себя идентично, за исключением некоторых условий:
1. `localStorage` один на всех вкладках в рамках одного истоничка, `sessionStorage` на каждой вкладке свой.
2. `localStorage` сохраняется после перезапуска браузера и ОС, `sessionStorage` пропадает даже после закрытия/открытия вкладки.

</p>
</details>

