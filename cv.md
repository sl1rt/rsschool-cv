# Barashkov Konstantin Mikhailovich

## Contacts
* Phone: +7 905 222 66 77
* Telegram: @dkagency
* Email: sl1rt@mail.ru

## About 
I like to create web-sites and interfaces.

## Skillset
* ⭐⭐⭐⭐⭐ HTML5 + Accessibility
* ⭐⭐⭐⭐⭐ CSS3 (SCSS)
* ⭐⭐⭐⭐📕 JavaScript
* ⭐⭐📕📕📕 PHP beginner

* Framework: Vue JS 2,3
* Utils: Git, Gulp, Docker, Postman
* Graphics: Figma, Adobe Photoshop, Adobe Illustrator

## Code example from codewars.com "How many nines?"

```javascript
let map = new Map();

const generateMap = (number, count = BigInt(0) ) => {
  let readyNum = map.get(number);
  if(readyNum) return readyNum;

  if(number.toString().length > 2) {
    count = number/10n + 9n*generateMap(number/10n);
  } else if(number.toString().length == 2) {
    count = 1n;
  }

  map.set(number, count)
  return count;
}

const nines = (maxNumber, count = 0n) => {
  let numString = maxNumber.toString();  
  let numLength = numString.length;
  let nextNotNull = 0;

  let makePow = Array.from({length: numLength-2 }).reduce((prev)=> {
    return prev*=10n;
  }, 10n)

  if(numLength == 1) {
    if(numString[0] == 9) {
      count += 1n;
    }
  } else {

    if(numString[0] == 9) {
      count += BigInt(numString.substring(1)) + 1n;
      count += 9n*generateMap(makePow);
      
      return count;
    }
    else
    {
      let pos = 1;
      while(pos < numString.length) {
        if(numString[pos] > 0) {
          nextNotNull = BigInt(numString.substring(pos));        
          break;
        }     
        pos ++;
      }
                  
      if(numString[0] != 0) {
        count += BigInt(numString[0])*generateMap(makePow); 
      }
      
      count += nines(nextNotNull);   
      
      return count;
    }  
  }
    
  return count;
}
```

## Work experience
I work for 8 years in freelance, developing web sites on CMS Modx Revolution.

## Education
St. Petersburg Technical College of Management and Commerce - Information Security

## Laguages
Russian - Native
English - A + read technical documentation