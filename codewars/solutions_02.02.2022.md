# CODEWARS

### TASK 1
###### https://www.codewars.com/kata/5b16490986b6d336c900007d/train/javascript

<img width="1280" alt="Screenshot 2022-02-02 at 10 24 09" src="https://user-images.githubusercontent.com/67319575/152111472-fad27c4a-a99e-46f1-b547-d682cd2d03b8.png">

```
function myLanguages(results) {
  let result = [];
  
  Object.entries(results).sort((a,b) => b[1] - a[1]).forEach((elem) => {
    if (elem[1] >= 60) {
      result.push(elem[0]);
    }
  })
  
  return result
}
```

### TASK 2
###### https://www.codewars.com/kata/585b1fafe08bae9988000314/train/javascript

<img width="1280" alt="Screenshot 2022-02-02 at 10 44 30" src="https://user-images.githubusercontent.com/67319575/152113516-87b70e88-448d-4e80-b222-fc46559c002a.png">

```
function explode(s) {
  let result = '';

  for(let i = 0; i < s.length; i++) {
    for(let j = 0; j < s[i]; j++) {
      result+=s[i];
    }
  }
  
  return result;
}
```

### TASK 3
###### https://www.codewars.com/kata/585b1fafe08bae9988000314/train/javascript

<img width="1280" alt="Screenshot 2022-02-02 at 11 06 03" src="https://user-images.githubusercontent.com/67319575/152116104-3e0dcccf-736d-4f85-851b-fe2009213fb9.png">

```
function nicknameGenerator(name){
  return name.length < 4 ? 'Error: Name too short' : /[a,e,i,o,u]/gi.test(name[2]) ? name.substr(0,4): name.substr(0,3);
}
```
