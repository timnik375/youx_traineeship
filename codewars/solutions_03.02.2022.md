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
  listeners = new Set();

  constructor(title, artist) {
    this.title = title;
    this.artist = artist;
  }
  
  howMany (arrListeners) {
    let counter = 0;
    arrListeners.forEach((elem) => {
      if (!this.listeners.has(elem.toLowerCase())) {
        counter++;
        this.listeners.add(elem.toLowerCase());
      };
    })
    
    return counter;
  }
}
```
