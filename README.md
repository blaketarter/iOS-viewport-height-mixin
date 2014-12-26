iOS-viewport-height-mixin
=========================

A sass mixin to handle viewport height quirkiness on iOS 7 and Below.

It generate a series of media queries to target the exact dimensions of various iOS devices.

##Usage


```
@include vh('height', 100, false);
```

Would be equivalent to...

```
height: 100vh;
```

The Mixin takes three parameters.
  - Property: String - _ie 'height' or 'max-height'_
    - Thee property you want to be generated.
  - Value: Number _ie 100 or 80_
    - The number of viewport units you want the element to take up.
  - Important: Boolean - _ie true or false_
    - Whether or not you want the generated property to have the !important flag.

##Example

```
.example {
  @include vh('max-height', 100, true);
}
```

Would output...

```
.example {
  max-height: 100vh !important;
}
@media all and (device-width: 768px) and (device-height: 1024px) and (orientation: portrait) {
  .example {
    max-height: 1024px !important;
  }
}
@media all and (device-width: 768px) and (device-height: 1024px) and (orientation: landscape) {
  .example {
    max-height: 768px !important;
  }
}
@media all and (device-width: 320px) and (device-height: 480px) and (orientation: portrait) {
  .example {
    max-height: 480px !important;
  }
}
@media all and (device-width: 320px) and (device-height: 480px) and (orientation: landscape) {
  .example {
    max-height: 320px !important;
  }
}
@media all and (device-width: 320px) and (device-height: 568px) and (orientation: portrait) {
  .example {
    max-height: 568px !important;
  }
}
@media all and (device-width: 320px) and (device-height: 568px) and (orientation: landscape) {
  .example {
    max-height: 320px !important;
  }
}
@media all and (device-width: 375px) and (device-height: 667px) and (orientation: portrait) {
  .example {
    max-height: 667px !important;
  }
}
@media all and (device-width: 375px) and (device-height: 667px) and (orientation: landscape) {
  .example {
    max-height: 375px !important;
  }
}
@media all and (device-width: 414px) and (device-height: 736px) and (orientation: portrait) {
  .example {
    max-height: 736px !important;
  }
}
@media all and (device-width: 414px) and (device-height: 736px) and (orientation: landscape) {
  .example {
    max-height: 414px !important;
  }
}

```
