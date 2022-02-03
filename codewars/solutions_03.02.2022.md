# CODEWARS

### TASK 1
###### https://www.codewars.com/kata/53f0f358b9cb376eca001079/train/javascript

<img width="1280" alt="Screenshot 2022-02-03 at 09 38 46" src="https://user-images.githubusercontent.com/67319575/152293589-1c9e71fb-5234-443b-acb2-82f641f3097e.png">

```
var Ball = function(ballType='regular') {
  this.ballType = ballType;
};
```
### TASK 2
###### https://www.codewars.com/kata/6089c7992df556001253ba7d/train/javascript

<img width="1280" alt="Screenshot 2022-02-03 at 18 20 49" src="https://user-images.githubusercontent.com/67319575/152372242-f0b1ca86-938b-4552-aef0-4a53b3acd388.png">

```
class Song {
  constructor(title, artist) {
    this.title = title;
    this.artist = artist;
    this.listeners = new Set();
  }
  
  howMany (arrListeners) {
    let prevDayListeners = this.listeners.size;
    arrListeners.forEach(elem => {this.listeners.add(elem.toLowerCase())})
    
    return this.listeners.size - prevDayListeners;
  }
}
```

### TASK 3
###### https://www.codewars.com/kata/56f935002e6c0d55fa000d92/train/javascript

<img width="1280" alt="Screenshot 2022-02-03 at 19 13 47" src="https://user-images.githubusercontent.com/67319575/152382266-305df67b-36bd-4759-b547-97b46bf877fb.png">

```
class Shark extends Animal {
  constructor(name,age,status) {
    super(name, age, 0, "shark", status);
  }
}

class Cat extends Animal {
  constructor(name,age,status) {
    super(name, age, 4, "cat", status);
  }
  
  introduce() {
    return super.introduce() + '  Meow meow!'
  }
}

class Dog extends Animal {
  constructor (name,age,status,master) {
    super(name, age, 4, "dog", status);
    this.master = master;
  }
  
  greetMaster() {
    return `Hello ${this.master}`;
  }
}
```

### TASK 4
###### https://www.codewars.com/kata/56fcc1ee45040039ab0016da/train/javascript

<img width="1280" alt="Screenshot 2022-02-03 at 19 53 59" src="https://user-images.githubusercontent.com/67319575/152390105-4884d995-3357-4ce9-9389-7b6dea812c5e.png">

```
class Cube {
  constructor(length) {
    this.length = length;
  }
  
  get surfaceArea () {
    return 6*Math.pow(this.length,2);
  }
  
  set surfaceArea (value) {
    this.length = Math.sqrt(value/6);
  }
  
  get volume () {
    return Math.pow(this.length,3);
  }
  
  set volume (value) {
    this.length = Math.cbrt(value);
  }
}
```
