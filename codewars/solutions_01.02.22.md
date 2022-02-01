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

