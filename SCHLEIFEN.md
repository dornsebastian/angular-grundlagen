# Schleifen in Angular

Der Einstieg in Angular ist leicht – jedoch gibt es viele verschiedene Varianten, die an das gleiche Ziel führen. 
Das ist auch bei den Schleifen nicht anderes.


## Schleifen Kontrollstrukturen in JavaScript bzw. TypeScrpit

### For

```typescript
const array: string[] = ['A', 'B', 'C', 'D', 'E'];

for (let i = 0; i < array.length; i++) {
    const item = array[i];
    console.log(i + ': ' +item);
}

// Konsolenausgabe:
// 0: A
// 1: B
// 2: C
// 3: D
// 4: E
```

### For-in (Objekte)

```typescript
const object = {vorname: 'Max', nachname: 'Musterman'};

for (const property of object) {
    console.log(property + ': ' + object[property]);
}

// Konsolenausgabe:
// vorname: Max
// nachname: Musterman
```

### For-of (Arrays)

```typescript
const array: string[] = ['A', 'B', 'C', 'D', 'E'];

for (const item of array) {
    console.log(item);
}

// Konsolenausgabe:
// A
// B
// C
// D
// E
```

### While
```typescript
let i = 0;

while (i < 3) {
    console.log(i);
    i++;
}

// Konsolenausgabe:
// 0
// 1
// 2
```

### Do-While
```typescript
let i = 0;

do {
    console.log(i);
    i++;
} while (i < 3)

// Konsolenausgabe:
// 0
// 1
// 2
```

## Schleifen als Callback

### forEach - Array.prototype.forEach()

```typescript
const array = ['A', 'B', 'C', 'D', 'E'];

array.forEach((item) => {
  console.log(item);
});

// Konsolenausgabe:
// A
// B
// C
// D
// E
```

### find - Array.prototype.find()
```typescript
const array = [7, 17, 8, 20, 32];

const found = array.find((item) => {
    return item > 18;
});

console.log(found);

// Konsolenausgabe:
// 20
```

### filter - Array.prototype.filter()
```typescript
const array = [7, 17, 8, 20, 32];

const result = array.find((item) => {
    return item > 18;
});

console.log(result);

// Konsolenausgabe:
// [20, 32]
```

## Schleifen im Template mit Direktiven

### *ngFor


```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'ngfor-example',
  template: `
 <ul>
  <li *ngFor="let item of list"> 
    {{ item }}
  </li>
 </ul>
 `
})
class NgForExampleComponent {
  people = ['A', 'B', 'C', 'D', 'E'];
}
```

