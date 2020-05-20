### Source
[30 seconds of code](https://www.30secondsofcode.org/js/s/unzip)

### Example
``` js
unzip([['a', 1, true], ['b', 2, false]]); // [['a', 'b'], [1, 2], [true, false]]
unzip([['a', 1, true], ['b', 2]]);       // [['a', 'b'], [1, 2], [true]]
```

<details>
  <summary>Solution</summary>
  
  ``` js
  const unzip = (arr) => arr.reduce(
    (acc, subArr) => (subArr.forEach( (el, i) => acc[i] ? acc[i].push(el) : acc[i] = [el] ), acc)
  , []);
  ```
</details>
