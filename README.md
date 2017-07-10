# Angular Infinite Scroller 

```shell
npm install ngx-inf-for intersection-observer
```
```js
import { InfiniteScrollerModule } from 'ngx-inf-for';
import 'intersection-observer';

@NgModule({
  imports: [ ToxicInfiniteScrollerModule ]
})
```
Since this lib makes heavy use of IntersectionObserver you will need to import the [pollyfill](https://github.com/WICG/IntersectionObserver/tree/gh-pages/polyfill) for reasonable [browser support](http://caniuse.com/#search=intersection)

```html
<ng-template infFor [infForOf]="items" (load)="loadMore()" let-item [infForTrackBy]="trackById">
  <div>{{item}}</div>
<ng-template>
```
Since [Angular does not support `@Output` binding in structual sugar syntax](https://github.com/angular/angular/issues/12121) we have to use it the more verbose syntax


