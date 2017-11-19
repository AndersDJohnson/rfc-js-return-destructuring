# rfc-js-return-destructuring
A proposal for JS shorthand to return from destructuring.

```js
const foo = async () => {
  { ok: { return bar } } = await axios.get('https://api.example.com')
}
```

or:

```js
const foo = async () => {
  return bar from { ok: { bar } } = await axios.get('https://api.example.com')
}
```

or:

```js
const foo = async () => {
  return bar in { ok: { bar } } = await axios.get('https://api.example.com')
}
```

or:

```js
const foo = async () => {
  return bar of { ok: { bar } } = await axios.get('https://api.example.com')
}
```

or:

```js
const foo = async () => {
  return from { ok: { bar } } = await axios.get('https://api.example.com')
}
```

Equivalent to:

```js
const foo = async () => {
  const { ok: { bar } } = await axios.get('https://api.example.com')
  return bar
}
```

or:

```js
const foo = async () => {
  return (await axios.get('https://api.example.com')).ok.bar
}
```
