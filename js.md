
# repeat an array n times

```js
new Array(100).fill([1, 2, 3]).flat()
```

# async functions with Array.map

```js
const arr = [1, 2, 3];

const asyncRes = await Promise.all(arr.map(async (i) => {
   await sleep(10);
   return i + 1;
}));
```

# 指数操作符

```js
2**10; // 1024
```
# Object.values()

```js
Object.values({a: 1, b: 2, c: 3}); // [1, 2, 3]
```

# Object.entries()

```js
Object.entries({a: 1, b: 2, c: 3}); // [["a", 1], ["b", 2], ["c", 3]]
```

# String padding

```js
// padStart
'hello'.padStart(10); // "     hello"
// padEnd
'hello'.padEnd(10) "hello     "
```


# 异步迭代

```js
async function process(array) {
  for await (let i of array) {
    // doSomething(i);
  }
}

```

# Nullish coalescing Operator

```js
let user = {
    u1: 0,
    u2: false,
    u3: null,
    u4: undefined
    u5: '',
}
let u2 = user.u2 ?? '用户2'  // false
let u3 = user.u3 ?? '用户3'  // 用户3
let u4 = user.u4 ?? '用户4'  // 用户4
let u5 = user.u5 ?? '用户5'  // ''
```

# Optional chaining

```js
let user = {}
let u1 = user.childer.name // TypeError: Cannot read property 'name' of undefined
let u1 = user.childer?.name // undefined
```

# Promise.allSettled

```js
const promise1 = Promise.resolve(3);
const promise2 = 42;
const promise3 = new Promise((resolve, reject) => reject('我是失败的Promise_1'));
const promise4 = new Promise((resolve, reject) => reject('我是失败的Promise_2'));
const promiseList = [promise1,promise2,promise3, promise4]
Promise.allSettled(promiseList)
.then(values=>{
  console.log(values)
});
```

# await with for...of

```js
async function process(array) {
  for await (let i of array) {
    // doSomething(i);
  }
}
```

# 数组去重
```js
const removeDuplicates = (arr) => [...new Set(arr)];
    
console.log(removeDuplicates([1, 2, 3, 3, 4, 4, 5, 5, 6]));
// Result: [ 1, 2, 3, 4, 5, 6 ]
```

# 从 URL 获取查询参数
```js
const getParameters = (URL) => {
  URL = JSON.parse(
    '{"' +
      decodeURI(URL.split("?")[1])
        .replace(/"/g, '\\"')
        .replace(/&/g, '","')
        .replace(/=/g, '":"') +
      '"}'
  );
  return JSON.stringify(URL);
};

getParameters(window.location);
// Result: { search : "easy", page : 3 }

---

Object.fromEntries(new URLSearchParams(window.location.search))
// Result: { search : "easy", page : 3 }

```

![image](https://user-images.githubusercontent.com/1579516/115391013-871e8480-a211-11eb-8564-a913d99f9b41.png)
