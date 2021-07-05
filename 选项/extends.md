**extends**

extends与mixins很像，不过extends只能扩展一个实例

执行顺序：extends>mixins

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
    <p>{{ num }}</p>
    <button @click="add">+</button>
  </div>
</body>

<script>
  let ex = {
    updated: function () {
      console.log(this.num);
    }
  }
  let vm = new Vue({
    el: '#app',
    data: {
      num: 1
    },
    methods: {
      add: function () {
        this.num++
      }
    },
    extends: ex
  })
</script>

</html>
```

