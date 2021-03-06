# Best Scroll ![version](https://img.shields.io/badge/version-%20v2.2.0%20-green.svg) ![vue](https://img.shields.io/badge/vue-%20v2.1%20-green.svg) 

## How to use

Download file[bestscroll](https://github.com/varjay/bestscroll/) , introduced in the code.

```js
import Vue from 'vue'
import scroll from 'best-scroll'
Vue.use(scroll)
```

```html
<scroller 
  :on-refresh="refresh"
  :on-infinite="infinite">
  <!-- content goes here -->
</scroller>
```

## API

#### Scroller component attributes:

| Attr. Name | Description | Required | Default Value |
|-----|-----|-----|-----|
| onRefresh | pull to refresh callback | N | - |
| onInfinite | infinite loading callback | N | - |
| onScroll | Y-axis position callback | N | - |
| refreshText | tips of `pull-to-refresh` | N | 下拉刷新 |
| noDataText | tips of `no-more-data` when `infinite-loading` finished | N | 没有更多数据 |
| width | scroller container width | N | `100%` |
| height | scroller container height | N | `100%` |
| snapping | enable snapping mode | N | `false` |
| snappingWidth | snapping width | N | 100 (stand for 100px) |
| snappingHeight | snapping height | N | 100 |
| refreshLayerColor | text color of `pull-to-refresh` layer | N | #AAA |
| loadingLayerColor | text color of `infinite-loading` layer | N | #AAA |
| minContentHeight | min content height (px) of `scroll-content` | N | 0 |

#### Scroller vm instance methods:

- `resize()` resize scroller content (**deprecated, cause the scroller's content resizes self automatically**)
- `triggerPullToRefresh()` start pull-to-refresh manually
- `finishPullToRefresh()` stop pull-to-refresh
- `finishInfinite(isNoMoreData :Boolean)` stop infinite-loading
- `scrollTo(x:Integer, y:Integer, animate:Boolean)` scroll to a position in scroller content
- `scrollBy(x:Integer, y:Integer, animate:Boolean)` scroll by a position in scroller content
- `getPosition :Object` get current position of scroller content
- `scrollElement(el, time, offsetX, offsetY, easing)` 
