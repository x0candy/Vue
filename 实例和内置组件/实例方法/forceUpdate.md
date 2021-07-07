**forceUpdate**

强制更新

之前提到过Vue.$set(),

通过数组下标改变数据，vue无法感知到，但数据是变化了的

可以用vue.$set(),

也可以用vue.$forceUpdate()强制更新

```vue
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <script src="https://cdn.jsdelivr.net/npm/vue/dist/vue.js"></script>
</head>

<body>
  <div id="app">
    <p>{{arr[0]}}</p>
    <button @click="add">+</button>
  </div>
</body>

<script>
  let app = new Vue({
    el: '#app',
    data: {
      arr: [1, 2, 3, 4, 5]
    },
    methods: {
      add: function () {
        this.arr[0] = 10 //vue无法感知到该数据变化
        this.$forceUpdate() //使用强制更新
      }
    },
  })
</script>

</html>
```

