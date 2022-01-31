# CODEWARS

### TASK 1
###### https://www.codewars.com/kata/52761ee4cffbc69732000738/train/javascript

<img width="1280" alt="Screenshot 2022-01-31 at 11 55 27" src="https://user-images.githubusercontent.com/67319575/151766491-bdaeb6a6-caf3-44b7-b54c-c693282f8bbf.png">

```
function goodVsEvil(good, evil) {
    let armyGood = 0;
    let armyEvil = 0;

    good.split(' ').forEach((elem, index) => {
        switch (index) {
            case 0:
                armyGood += elem * 1;
                break;
            case 1:
                armyGood += elem * 2;
                break;
            case 2:
                armyGood += elem * 3;
                break;
            case 3:
                armyGood += elem * 3;
                break;
            case 4:
                armyGood += elem * 4;
                break;
            case 5:
                armyGood += elem * 10;
                break;
        }
    });

    evil.split(' ').forEach((elem, index) => {
        switch (index) {
            case 0:
                armyEvil += elem * 1;
                break;
            case 1:
                armyEvil += elem * 2;
                break;
            case 2:
                armyEvil += elem * 2;
                break;
            case 3:
                armyEvil += elem * 2;
                break;
            case 4:
                armyEvil += elem * 3;
                break;
            case 5:
                armyEvil += elem * 5;
                break;
            case 6:
                armyEvil += elem * 10;
                break;
        }
    });

    if (armyGood > armyEvil) {
        return 'Battle Result: Good triumphs over Evil';
    } else if (armyGood < armyEvil) {
        return 'Battle Result: Evil eradicates all trace of Good';
    } else {
        return 'Battle Result: No victor on this battle field';
    }
}
```

### TASK 2
###### https://www.codewars.com/kata/your-order-please/train/javascript

<img width="1280" alt="Screenshot 2022-01-31 at 13 00 14" src="https://user-images.githubusercontent.com/67319575/151773717-549f4e28-cbbe-47b0-934b-242d3fd89012.png">

```
function order(words){
    let arr = words.split(' ');
    let arrLength = arr.length;
  
    if (arrLength === 0) {
      return ' ';
    }
  
    for (let i = 0; i < arrLength-1; i++) {
      for (let j = 0; j < arrLength-1-i; j++) {
        if (arr[j+1].match(/\d+/) < arr[j].match(/\d+/)) {
          let t = arr[j+1]; arr[j+1] = arr[j]; arr[j] = t;
        }
      }
     }                     
    return arr.join(' ');
}
```

### TASK 3
###### https://www.codewars.com/kata/does-my-number-look-big-in-this/train/javascript

<img width="1280" alt="Screenshot 2022-01-31 at 13 30 47" src="https://user-images.githubusercontent.com/67319575/151778062-2a3e357d-a12a-4091-a2b7-36dc93a14d85.png">

```
function narcissistic(value) {
  let degree = String(value).length;
  let numNew = 0;
  
  String(value).split('').forEach((elem) => {
    numNew += Math.pow(elem, degree);
  })
  
  return value === numNew ? true : false;
}
```

### TASK 4
###### https://www.codewars.com/kata/array-helpers/train/javascript

<img width="1280" alt="Screenshot 2022-01-31 at 14 50 42" src="https://user-images.githubusercontent.com/67319575/151789274-c9a26d02-8de3-44fd-92a6-9d7e78ac0966.png">

```
Array.prototype.square = function () {
  let result = [];
  this.forEach((elem) => {
    result.push(Math.pow(elem, 2));
  })
  
  return result;
}

Array.prototype.cube = function () {
  let result = [];
  this.forEach((elem) => {
    result.push(Math.pow(elem, 3));
  })
  
  return result;
}

Array.prototype.sum = function () {
  let result = 0;
  this.forEach((elem) => {
    result += elem;
  })
  
  return result;
}

Array.prototype.average = function () {
  return this.sum()/this.length;
}

Array.prototype.even = function () {
  let result = [];
  this.forEach((elem) => {
    if (elem%2 === 0) {
      result.push(elem)
    }
  })
  
  return result;
}

Array.prototype.odd = function () {
  let result = [];
  this.forEach((elem) => {
    if (elem%2 !== 0) {
      result.push(elem)
    }
  })
  
  return result;
}
```

### TASK 5
###### https://www.codewars.com/kata/pete-the-baker/train/javascript

<img width="1280" alt="Screenshot 2022-01-31 at 16 04 03" src="https://user-images.githubusercontent.com/67319575/151798632-1d5ded40-a841-4dfc-9849-a99492a734d1.png">

```
function cakes(recipe, available) {
  let result = [];
  for (key in recipe) {
    result.push(Math.floor(available[key]/recipe[key]));
  }
  
  result.sort((a, b) => a - b);
  
  return isNaN(result[0])? 0: result[0];
}
```

### TASK 6
###### https://www.codewars.com/kata/525f3eda17c7cd9f9e000b39/train/javascript

<img width="1280" alt="Screenshot 2022-01-31 at 17 47 20" src="https://user-images.githubusercontent.com/67319575/151814708-f923506e-498e-498f-b37d-edcad9cfc0ba.png">

```
function getValue(callback, num) {
    return typeof callback === 'function' ? callback(num) : num;
}

function zero(callback) {
  let num = 0;
  return getValue(callback, num);
}
function one(callback) {
  let num = 1;
  return getValue(callback, num);
}
function two(callback) {
  let num = 2;
  return getValue(callback, num);
}
function three(callback) {
  let num = 3;
  return getValue(callback, num);
}
function four(callback) {
  let num = 4;
  return getValue(callback, num);
}
function five(callback) {
  let num = 5;
  return getValue(callback, num);
}
function six(callback) {
  let num = 6;
  return getValue(callback, num);
}
function seven(callback) { 
  let num = 7;
  return getValue(callback, num);
}
function eight(callback) {
  let num = 8;
  return getValue(callback, num);
}
function nine(callback) {
  let num = 9;
  return getValue(callback, num);
}

function plus(x) {
  return function (y) {
    return x + y;
  }
}
function minus(x) {
  return function (y) {
    return y - x;
  }
}
function times(x) {
  return function (y) {
    return x * y;
  }
}
function dividedBy(x) {
  return function (y) {
    return Math.floor(y/x);
  }
}
```
