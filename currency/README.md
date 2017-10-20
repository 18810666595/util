### 过滤器，格式化金额

使用方法例子：
```
currency (value, currency, decimals)

/**
  接受三个参数，
  第一个参数为格式化的数字，在下面例子中默认为 totalPrice.
  第二个为前缀的金额符号,String 类型，默认为 '$'
  第三个为小数位数，Number 类型，默认为 2 位小数
```
### .vue 文件中
```
//  <template> 文件

{{ totalPrice | currency("$") }}  
```
```
// <script> 文件

import {currency} from '**/util/currency.js'

export default {
  data() {
    return {
      totalPrice: 12345
    }
  },
  filters: {
    currency: currency
  }
}
```
```
//输出效果为

$12,345.00
```
