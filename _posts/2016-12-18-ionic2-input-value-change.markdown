---
layout: post
title:  "Ionic 2 : How to detect value change in ion-input"
date:   2016-12-18 18:43:18 +0200
categories: angular2
---

## How to detect value change in ion-input
Utiliser (input) plutôt que :
 * (change) qui ne se déclenche que sur perte du focus
 * (keypress) qui ne prend pas en compte les retours arrière
 
### HTML template
```HTML
<ion-input [(ngModel)]="myField" (input)="onChange($event.target.value)"></ion-input>
```

### Component 
```javascript
onChange(value) {
    // value is the input content;
}
```