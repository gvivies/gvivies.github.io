---
layout: post
title:  "Attributs injectes"
date:   2016-09-04 23:48:18 +0200
categories: angular2
---

## 2 façons d'injecter les services par exemple :

### directement dans le constructeur

```javascript
export class MonComposant {

  constructor(private http: Http) {}
  
  method(): any {
   this.http....
  }
```


### en déclarant un attribut 

```javascript
export class MonComposant {
  
  private myHttp: Http;
 
  constructor(http: Http) {
    this.myHttp = http;
  }
  
  method(): any {
    this.myHttp....
  }
```