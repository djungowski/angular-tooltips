# ng-tooltips

Tooltips for any element using any html in AngularJS with no requirements. This is a fork of [angular-tooltips](https://github.com/Intellipharm/angular-tooltips), 
replacing the `title` attribute with `tooltip`, since using `title` directly can cause various problems, especially if you
use another directive which depends on the title attribute.

**Why another tooltip library?**

There are other libraries out there like https://github.com/720kb/angular-tooltips or https://angular-ui.github.io/bootstrap/#/tooltip
but they either have requirements on other libraries or are overly convoluted in their approach (which can break other things).

This is a very small (8 kB) library that keeps things simple. It also cleans up after itself and doesn't leave rouge elements all over the window.

## Installation

Install through yarn or npm

```
npm install --save ng-tooltips
```

```
yarn add ng-tooltips
```

Include the library files

```html
<link rel="stylesheet" href="node_modules/ng-tooltips/dist/angular-tooltips.css" />
<script src="node_modules/ng-tooltips/dist/angular-tooltips.js"></script>
```

Add the angular model ```tooltips```

```js
angular.module('app', ['ng-tooltips'])
```

## Usage

Just add a tooltip attribute.

```html
<i class="fa fa-star" tooltip="This is a star!"></i>
```

The direction of the tooltip can be specified using ```tooltip-direction``` with the options: top, top-right, right-top, right, right-bottom, bottom-right, bottom, bottom-left, left-bottom, left, left-top, top-left

```html
<i class="fa fa-star" tooltip="This is a star!" tooltip-direction="right"></i>
```

The direction of the tooltip will automatically swap if the tooltip will sit outside of the window bounds.
To stop this happening and force the direction set the ```tooltip-fixed-position``` option

```html
<i class="fa fa-star" tooltip="This is a star!" tooltip-direction="right" tooltip-fixed-position="true"></i>
```

## Demo

http://intellipharm.github.io/angular-tooltips/

## Requrements

**None!!**
