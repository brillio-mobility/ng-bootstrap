# NG Bootstrap - [Angular](http://angular.io/)


Welcome to the Angular version of the [Angular UI Bootstrap](https://github.com/angular-ui/bootstrap) library with support for Bootstrap 3.0.


## Table of Contents

- [Demo](#demo)
- [Dependencies](#dependencies)
- [Installation](#installation)
  - [SystemJS](#systemjs)
- [Supported browsers](#supported-browsers)
- [You think you've found a bug?](#you-think-youve-found-a-bug)
- [Code of Conduct](#code-of-conduct)


## Dependencies
* [Angular](https://angular.io) (tested with 4.0.3)

## Installation
After installing the above dependencies, install `ng-bootstrap` via:
```shell
npm install --save ng-bootstrap-brillio
```
Once installed you need to import our main module:
```js
import {NgbModule} from 'ng-bootstrap-brillio';
```
The only remaining part is to list the imported module in your application module. The exact method will be slightly
different for the root (top-level) module for which you should end up with the code similar to (notice `NgbModule.forRoot()`):
```js
import {NgbModule} from 'ng-bootstrap-brillio';

@NgModule({
  declarations: [AppComponent, ...],
  imports: [NgbModule.forRoot(), ...],
  bootstrap: [AppComponent]
})
export class AppModule {
}
```

Other modules in your application can simply import `NgbModule`:

```js
import {NgbModule} from 'ng-bootstrap-brillio';

@NgModule({
  declarations: [OtherComponent, ...],
  imports: [NgbModule, ...],
})
export class OtherModule {
}
```

### SystemJS
If you are using SystemJS, you should also adjust your configuration to point to the UMD bundle.

In your systemjs config file, `map` needs to tell the System loader where to look for `ng-bootstrap`:
```js
map: {
  'ng-bootstrap-brillio': 'node_modules/ng-bootstrap-brillio/bundles/ng-bootstrap.js',
}
```
## Supported browsers

We support the same browsers and versions supported by both Bootstrap 4 and Angular, whichever is _more_ restrictive.
See [this](https://github.com/angular/angular/blob/master/README.md) for up-to-date Angular browser support.

* Chrome (45+)
* Firefox (40+)
* IE (10+)
* Edge (20+)
* Safari (7+)


## You think you've found a bug?

Oh, we are ashamed and want to fix it ASAP! But before fixing a bug we need to reproduce and confirm it. In order to reproduce bugs we will systematically ask you to provide a _minimal_ reproduction scenario using http://plnkr.co. Having a live, reproducible scenario gives us wealth of important information without going back & forth to you with additional questions like:
* version of Angular used
* version of this library that you are using
* 3rd-party libraries used, if any
* and most importantly - a use-case that fails

A minimal reproduce scenario using http://plnkr.co/ allows us to quickly confirm a bug (or point out coding problem) as well as confirm that we are fixing the right problem.
The best part is that you do not need to create plunks from scratch - you can fork one from our [demo page](https://ng-bootstrap.github.io/#/components).

We will be insisting on a minimal reproduce scenario in order to save maintainers time and ultimately be able to fix more bugs. Interestingly, from our experience users often find coding problems themselves while preparing a minimal plunk. We understand that sometimes it might be hard to extract essentials bits of code from a larger code-base but we really need to isolate the problem before we can fix it.

Unfortunately we are not able to investigate / fix bugs without a minimal reproduce scenario using http://plnkr.co, so if we don't hear back from you we are going to close an issue that don't have enough info to be reproduced.

## Code of Conduct

Please take a moment and read our [Code of Conduct](CODE_OF_CONDUCT.md)
