### Sources
> [30 seconds of code](https://www.30secondsofcode.org/js/t/array/a/2/)

### Desciption

``` js
 JSONtoCSV([{ a: 1, b: 2 }, { a: 3, b: 4, c: 5 }, { a: 6 }, { b: 7 }], ['a', 'b']); 
```

### Result

``` js
"a,b
"1","2"
"3","4"
"6",""
"","7""
```


<details>
  <summary><strong> Solution </strong></summary>
  
``` js
const JSON_To_CSV = (objPairArr, objKeyArr) => objPairArr.reduce(
(acc, el) => acc + "\n" + objKeyArr.map((key) => el[key] ? `"${el[key]}"` : `""`).join()
, objKeyArr.join());
```
  
</details>
