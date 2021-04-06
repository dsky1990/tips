
# repeat an array n times

```
new Array(100).fill([1, 2, 3]).flat()
```

# async functions with Array.map

```
const arr = [1, 2, 3];

const asyncRes = await Promise.all(arr.map(async (i) => {
	await sleep(10);
	return i + 1;
}));
```
