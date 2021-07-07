**off**

关闭事件

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
    <p>{{num}}</p>
    <button @click="$emit('add')">+</button>
  </div>
  <button onclick="off()">off</button>
</body>

<script>
  let app = new Vue({
    el: '#app',
    data: {
      num: 1
    }
  })
  app.$on('add', function () {
    this.num++
  })

  function off() {
    app.$off('add')
  }
</script>

</html>
```

