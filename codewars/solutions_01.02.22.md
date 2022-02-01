# CODEWARS

### TASK 1
###### https://www.codewars.com/kata/52761ee4cffbc69732000738/train/javascript

<img width="1280" alt="Screenshot 2022-02-01 at 14 27 49" src="https://user-images.githubusercontent.com/67319575/151961595-9645b8a0-0611-42cf-b39b-514b315fb420.png">

```
tree.prototype.describe = function () {
  return `This tree has ${this.trunks} trunks, ${this.branches} branches, ${this.twigs} twigs and ${this.leaves} leaves.`
}

tree.prototype.chopTrunk = function (n) {
  this.trunks = this.trunks - n <= 0? 0 : this.trunks - n;
  this.branches = this.branches - n*10 <= 0? 0 : this.branches - n*10;
  this.twigs = this.twigs - n*100 <= 0? 0 : this.twigs - n*100;
  this.leaves = this.leaves - n*1000 <= 0? 0 : this.leaves - n*1000;
}

tree.prototype.chopLeaf = function (n) {
  this.leaves = this.leaves - n <= 0? 0 : this.leaves - n;
}

tree.prototype.chopTwig = function (n) {
  this.twigs = this.twigs - n <= 0? 0 : this.twigs - n;
  this.leaves = this.leaves - n*10 <= 0? 0 : this.leaves - n*10;
}

tree.prototype.chopBranch = function (n) {
  this.branches = this.branches - n <= 0? 0 : this.branches - n;
  this.twigs = this.twigs - n*10 <= 0? 0 : this.twigs - n*10;
  this.leaves = this.leaves - n*100 <= 0? 0 : this.leaves - n*100;
}
```

### TASK 2
###### https://www.codewars.com/kata/57f625992f4d53c24200070e/solutions/javascript

<img width="1280" alt="Screenshot 2022-02-01 at 15 21 24" src="https://user-images.githubusercontent.com/67319575/151967775-a1cd3b60-464c-426f-ba17-47ddf30c5bce.png">

```
function bingo(ticket, win){
  let winCounter = 0;
  
  ticket.forEach((elem) => {
    for (let i = 0; i < elem[0].length; i++) {
      if (elem[0].charCodeAt(i) === elem[1]) {
        winCounter++;
        i = elem[0].length;
      }
    }
  })
  
  
  return winCounter >= win ? 'Winner!' : 'Loser!';
}
```


### TASK 3
###### https://www.codewars.com/kata/513e08acc600c94f01000001/train/javascript

<img width="1280" alt="Screenshot 2022-02-01 at 16 25 17" src="https://user-images.githubusercontent.com/67319575/151976684-9e7a2a4a-1384-4124-9751-a84eeed75b3d.png">

```
function rgb(r, g, b){
  let color = '';
  
  for(let i = 0; i < arguments.length; i++) {
    color += numConvert(arguments[i]);
  }

  return color;
}

function numConvert (num) {
  let result = '';
  
  num = Number(num);
  
  if (num <= 0) {
    return result += '00';
  }
  
  if (num >= 255) {
    return result += 'FF';
  }
  
  const hexArr = [0,1,2,3,4,5,6,7,8,9,'A','B','C','D','E','F']
  
  if (num/16 !== 0) {
    result += hexArr[Math.floor(num/16)];
    result += hexArr[num%16];
    
    return result;
  } else {
    result += hexArr[num];
    result += hexArr[num];
    
    return result;
  }
}
```

### TASK 4
###### https://www.codewars.com/kata/554e4a2f232cdd87d9000038/train/javascript

<img width="1280" alt="Screenshot 2022-02-01 at 16 41 46" src="https://user-images.githubusercontent.com/67319575/151979187-f16924d8-fc6b-4d64-b8e5-b6dc1cee6a73.png">

```
function DNAStrand(dna){
  return dna.split('').map(item => item === 'A'? 'T' : item === 'T' ? 'A' : item === 'G' ? 'C': item === 'C'? 'G' : item).join('');  
}
```

### TASK 5
###### https://www.codewars.com/kata/529f32794a6db5d32a00071f/train/javascript

<img width="1280" alt="Screenshot 2022-02-01 at 16 55 00" src="https://user-images.githubusercontent.com/67319575/151981447-8409ba40-e199-4b02-ba57-62c8fd601596.png">

```
var Calculator = {
 average: function(...args) {
   return args.length === 0 ? 0: args.reduce((sum, current) => sum + current)/args.length
 }
};
```

### TASK 6
###### https://www.codewars.com/kata/5a2cb4bff28b820c33000082/train/javascript

<img width="1280" alt="Screenshot 2022-02-01 at 18 03 17" src="https://user-images.githubusercontent.com/67319575/151993664-e0f11a4b-abca-407c-9376-c42faba3e162.png">

```
function whoseBicycle(...args) {
  let result = [];
  
  args.forEach((elem) => {
    result.push(Object.values(elem).reduce((sum, cur) => sum + cur))
  })

  let sonNum = null;
  let sonHighScore = 0;
  
  result.forEach((elem, index) => {
    if (elem > sonHighScore) {
      sonNum = index;
      sonHighScore = elem;
    }
    
    if (elem === sonHighScore) {
        sonNum = Object.values(ageTable)[sonNum] < Object.values(ageTable)[index] ? sonNum : index;
        sonHighScore = Object.values(ageTable)[sonNum] < Object.values(ageTable)[index] ? sonHighScore : elem;
    }
  })

  switch(sonNum) {
    case 0:
      return 'I need to buy a bicycle for my first son.';
    case 1:
      return 'I need to buy a bicycle for my second son.';
    case 2:
      return 'I need to buy a bicycle for my third son.';
  }
}
```

### TASK 7
###### https://www.codewars.com/kata/525f50e3b73515a6db000b83/train/javascript

<img width="1280" alt="Screenshot 2022-02-01 at 18 15 32" src="https://user-images.githubusercontent.com/67319575/151995843-92f8facd-ba99-4d7c-bc89-ffab365a75d0.png">

```
function createPhoneNumber(numbers){
  let firstPart = '';
  let secondPart = '';
  let thirdPart = '';
  
  numbers.forEach((elem, index) => {
    if (index < 3) {
      firstPart += elem;
    } else if (index < 6) {
      secondPart += elem;
    } else {
      thirdPart += elem;
    }
  })
  
  return `(${firstPart}) ${secondPart}-${thirdPart}`;
}
```
