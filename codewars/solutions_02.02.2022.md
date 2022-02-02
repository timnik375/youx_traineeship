# CODEWARS

### TASK 1
###### https://www.codewars.com/kata/5b16490986b6d336c900007d/train/javascript

<img width="1280" alt="Screenshot 2022-02-02 at 10 24 09" src="https://user-images.githubusercontent.com/67319575/152111472-fad27c4a-a99e-46f1-b547-d682cd2d03b8.png">

```
  let result = [];
  
  Object.entries(results).sort((a,b) => b[1] - a[1]).forEach((elem) => {
    if (elem[1] >= 60) {
      result.push(elem[0]);
    }
  })
  
  return result
```

