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
