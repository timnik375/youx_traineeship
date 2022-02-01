# CODEWARS

### TASK 1
###### https://www.codewars.com/kata/52761ee4cffbc69732000738/train/javascript



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
