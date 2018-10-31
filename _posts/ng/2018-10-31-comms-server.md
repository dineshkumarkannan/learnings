---
title:  "Communicating with the Server"
date:   2018-10-31 05:30:00 +0530
categories: ng
---

## HTTP

```js
/**
 *  some.service.ts
 */
...
import { HttpClient } from '@angular/common/http';
...
export class SomeService {
    constructor(private http: HttpClient) {}
    ...
}

/**
 *  app.module.ts
 */
...
import { HttpClientModule } from '@angular/common/http';
...
@NgModule({
    imports: [
        ...,
        HttpClientModule
    ],
    ...
})
...
```

## HTTP - Get, Post, Put and Delete

```js
/**
 *  some.service.ts
 */
...
import { Observable } from 'rxjs';
import { HttpClient } from '@angular/common/http';
...
export class SomeService {
    constructor(private http: HttpClient) {}
    ...
}
```
