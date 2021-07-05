**watch**

监听数据变化

可以脱离构造器，降低代码耦合性



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
    <input type="text">
    <button @click="add">+</button>
  </div>
</body>

<script>
  let vm = new Vue({
    el: '#app',
    data: {
      x: 1,
      y: 1,
      z: 1
    },
    methods: {
      add: function () {
        this.x++
      }
    },
  })
  vm.$watch('x', function () {
    this.y++,
      this.z++
  })
</script>

</html>
```

