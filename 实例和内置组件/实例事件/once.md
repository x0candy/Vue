**once**

跟on差不多，但once自定义的事件只能执行一次，随后就被移除

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
</body>

<script>
  let app = new Vue({
    el: '#app',
    data: {
      num: 1
    }
  })
  app.$once('add', function () {
    this.num++
  })
</script>

</html>
```

