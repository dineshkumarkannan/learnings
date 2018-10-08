---
title:  "Angular app Structure"
date:   2018-10-02 16:43:00 +0530
categories: ng
---

## App module:

  ```js
  /**
   *  app.module.ts
   */
  import { NgModule } from '@angular/core';
  ...
  @NgModule({
      imports: [
        // modules
        // components
      ],
      declarations: [
        // dirctives
        // pipes
      ],
      providers: [
        // services
      ],
      exports: [
        // component
      ],
      bootstrap: [
        // root component
      ]
  })

  export class AppModule { }
  ```

## Component:

  ```js
  /**
   *  some.component.ts
   */
  import { Component } from '@angular/core';
  ...
  @Component({
      selector: 'app-some-component',

      /** including component template */
      templateUrl: `
        // path to external template
      `,
      /** or */
      template: `
        // inline template
      `,

      /** including component styles */
      styleUrls: [
        // paths to external stylesheets
      ],
      /** or */
      styles: [
        // array of inline styles
      ]
  })
  
  export class SomeComponent {
      ...
  }
  ```
