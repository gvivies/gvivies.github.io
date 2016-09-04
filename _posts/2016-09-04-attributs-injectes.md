# Déclaration et utilisations des éléments injectés :

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