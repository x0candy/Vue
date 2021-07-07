**on**

监听自定义事件,大白话：在构造器外部自定义事件

app.$on('事件名',回调函数)

使用emit来触发事件

app.$emit('事件名',[...arg])

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
  app.$on('add', function () {
    this.num++
  })
</script>

</html>
```

