<style>
.demo-layout {
  .van-row {
    padding: 0 15px;
  }
  .van-col {
    color: #fff;
    font-size: 13px;
    line-height: 30px;
    text-align: center;
    margin-bottom: 10px;
    background-clip: content-box;

    &:nth-child(odd) {
      background-color: #39a9ed;
    }

    &:nth-child(even) {
      background-color: #66c6f2;
    }
  }
}
</style>

## Layout

Quickly and easily create layouts with `van-row` and `van-col`

### Install
``` javascript
import { Row, Col } from 'vant';

Vue.component(Row.name, Row);
Vue.component(Col.name, Col);
```

### Usage

#### Basic

Layout are based on 24-column. The attribute `span` in `Col` means the number of column the grid spans. Of course, You can use `offset` attribute to set number of spacing on the left side of the grid.

:::demo Basic Usage
```html
<van-row>
  <van-col span="8">span: 8</van-col>
  <van-col span="8">span: 8</van-col>
  <van-col span="8">span: 8</van-col>
</van-row>

<van-row>
  <van-col span="4">span: 4</van-col>
  <van-col span="10" offset="4">offset: 4, span: 10</van-col>
  <van-col span="6">span: 6</van-col>
</van-row>

<van-row>
  <van-col offset="12" span="12">offset: 12, span: 12</van-col>
</van-row>
```
:::

#### Column Spacing

Set grid spacing using `gutter` attribute. The default value is 0

:::demo Column Spacing
```html
<van-row gutter="20">
  <van-col span="8">span: 8</van-col>
  <van-col span="8">span: 8</van-col>
  <van-col span="8">span: 8</van-col>
</van-row>
```
:::

### API

#### Row
| Attribute       | Description      | Type       | Default       | Accepted Values       |
|-----------|-----------|-----------|-------------|-------------|
| gutter | grid spacing（px） | `String | Number` | - | - |
| prefix | className prefix | `String` | `van` | - |

#### Column
| Attribute       | Description      | Type       | Default       | Accepted Values       |
|-----------|-----------|-----------|-------------|-------------|
| span | number of column the grid spans | `String | Number`  | - | - |
| offset | number of spacing on the left side of the grid | `String | Number` | -  | - |
| prefix | className prefix | `String`  | `van` | - |
