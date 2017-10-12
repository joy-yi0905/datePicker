# datePicker

一款基于zepto的日期选择，可适用于移动端（主要）和PC端。

datePicker演示：**[demo](http://joy-yi0905.github.io/datePicker/demo/demo.html)**

### 如何使用

- 首先引入插件的样式 `zepto.datepicker.min.css`

```html
<link rel="stylesheet" href="src/zepto.datepicker.min.css">
```

- 然后再引入 `zepto.min.js` 和 `zepto.datepicker.min.js`（demo目录已压缩）

```html
<script src="src/zepto.min.js"></script>
<script src="src/zepto.datepicker.min.js"></script>
```

- 最后在页面里，为需要的 `<input>` 元素添加方法。 相关示例代码：

```html
<input type="text" placeholder="请选择日期" class="input-date" />

<script>
$('.input-date').datePicker();
</script>
```

除此之外，datePicker 还提供了 `type`、`date` `yearCols` 等一些自定义属性。你可以像这样配置它们：

```js
$('.input-date-custom').datePicker({
  date: '2015-05-01',
  callback: (date) => {
    console.log(date);
  }
})
```

上面的代码表示，用户自定义了日期 `2015-05-01`，并且每次选择完，将回调输出输入框的日期。

相关参数的具体使用，详见下表。

### 参数

datePicker 相关参数配置如下：

| **参数** | **描述** | **默认值** | **格式** |
|----------|----------|------------|----------|
| type | 日期类型 | `date` | 字符串，你也可设置 `date-time`，表示包含时分 |
| date | 初始日期 | 当前时间 | YYYY-MM-DD hh:ss |
| titleDisplay | 是否显示头部 | true | 布尔值 |
| yearCols | 可选的年份 | [2000, ..., 2030] | 数组 |
| monthCols | 可选的月份 | [01, ..., 12] | 数组 |
| dayCols | 可选择的天 | [01, ..., 31] | 数组 |
| hourCols | 可选择的小时 | [00, ..., 23] | 数组 |
| minuteCols | 可选择的分钟 | [00, ..., 59] | 数组 |
| callback | 每次选择后的回调 | 空函数 | 参数为选择后的日期 |

