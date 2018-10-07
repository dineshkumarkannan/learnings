---
title:  "Styling components"
date:   2018-10-02 17:23:00 +0530
categories: ng
---

## Using **[ngStyle]**:

  ```html
  ...
  <div [ngStyle]="{ 'color': red }"></div>
  ...
  ```

## Using **[class]**:

  ```html
  ...
  <div [class.class-1]="booleanParam" [class.class-2]="funcReturningBoolean()"></div>
  ...
  ```

## Using **[ngClass]**:

  ```html
  ...
  <div [ngClass]="{
      'class-1': booleanParam,
      'class-2 class-3': funcReturningBoolean()
      }">
  </div>
  ...
  ```
