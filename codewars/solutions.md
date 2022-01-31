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
