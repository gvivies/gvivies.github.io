---
layout: post
title:  "angular2 RC5 Http TypeError: Cannot read property toString of undefined"
date:   2016-09-05 23:48:18 +0200
categories: angular2
---

## TypeError: Cannot read property 'toString' of undefined

Lors de l'utilisation du service http.get() avec utilisation de header, on obtient l'erreur car le body est null.

### workaround 
Passer le body vide si besoin d'un header :

```javascript
this.http.get(url, { headers : headers, body: '' }). ...
```