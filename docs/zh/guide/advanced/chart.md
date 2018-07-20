# 图表



管理后台图表也是常见得需求。这里图表就只推荐 v-charts，功能齐全，社区 demo 也丰富 [v-charts](https://v-charts.js.org/)。

在使用echarts生成图表时，经常需要做繁琐的数据类型转化、修改复杂的配置项，v-charts的出现正是为了解决这个 痛点。基于Vue2.0和echarts封装的v-charts图表组件，只需要统一提供一种对前后端都友好的数据格式 设置简单的配置项，便可轻松生成常见的图表。


安装
```js
npm i v-charts echarts -S
```
引入 （在main.js里面引入）
```js
import VCharts from 'v-charts'
```

快速上手
```js
<template>
  <div>
    <ve-line :data="chartData"></ve-line>
  </div>
</template>

<script>
import VeLine from 'v-charts/lib/line'
export default {
  created () {
    this.chartData = {
      columns: ['日期', '销售量'],
      rows: [
        { '日期': '1月1日', '销售量': 123 },
        { '日期': '1月2日', '销售量': 1223 },
        { '日期': '1月3日', '销售量': 2123 },
        { '日期': '1月4日', '销售量': 4123 },
        { '日期': '1月5日', '销售量': 3123 },
        { '日期': '1月6日', '销售量': 7123 }
      ]
    }
  },

  components: { VeLine }
}
</script>
```


其实都差不多，还是要结合自己业务来封装。后面就和平时使用 ECharts 没有什么区别了。题外话 ECharts 的可配置项真心多，大家使用的时候可能要花一点时间了解它的 api 的。知乎有个问题：百度还有什么比较良心的产品？答案：ECharts，可见 ECharts 的强大与好用。

## Demo
![](https://mgbq.github.io/onlinePreview/nxmin-charts.gif)

::: tip
具体实例可参照 `@/views/chart/` 文件下几个 chart 文件
:::

## 其它

当然社区里的其它图表如 [d3](https://github.com/d3/d3) , [Chart.js](https://github.com/chartjs/Chart.js) , [chartist-js](https://github.com/gionkunz/chartist-js) 等封装方法都是大同小异差不多的，这里就不再展开了。
