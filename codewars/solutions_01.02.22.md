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
