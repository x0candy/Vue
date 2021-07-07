**nextTick**

与updated类似，data里的参数修改完成后会调用nextTick

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
    <button @click="add">+</button>
  </div>
</body>

<script>
  let app = new Vue({
    el: '#app',
    data: {
      num: 1
    },
    methods: {
      add: function () {
        this.num++
        app.$nextTick(function () {
          console.log('+');
        })
      }
    },
  })
</script>

</html>
```

