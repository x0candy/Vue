**computed**

计算属性

主要是处理复杂逻辑

比如插值表达式中，{{ str.split('').reverse().join('') }} 反转字符串

对于这种逻辑复杂的表达式，我们就可以用computed

处理之后  {{ reverseStr }} 这样就可以一眼看出来是反转字符串



computed与方法的区别

computed只要原始数据没有改变，那么不管怎么调用，得到的都是缓存的数据

方法，调用一次，计算一次

```vue
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
  <title>Document</title>
</head>

<body>
  <div id="app" message="asd">
  </div>
</body>

<script>
  var newsList = [{
      title: '香港或就“装甲车被扣”事件追责 起诉涉事运输公司',
      date: '2017/3/10'
    },
    {
      title: '日本第二大准航母服役 外媒：针对中国潜艇',
      date: '2017/3/12'
    },
    {
      title: '中国北方将有明显雨雪降温天气 南方阴雨持续',
      date: '2017/3/13'
    },
    {
      title: '起底“最短命副市长”：不到40天落马，全家被查',
      date: '2017/3/23'
    },
  ];
  let app = Vue.extend({
    template: `<div><p v-for="item in news">{{item}}</p></div>`,
    data: function () {
      return {
        message: "asd",
        newList: newsList
      }
    },
    props: ['a'],
    computed: {
      news: function () {
        return this.newList.reverse()
      }
    }
  })
  new app({
    propsData: {
      a: 1
    }
  }).$mount('#app')
</script>

</html>
```

