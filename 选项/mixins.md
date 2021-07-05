**mixins**

混入组件选项，提高代码复用性

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
    <p>{{x}}</p>
    <button @click="add">+</button>
  </div>
</body>

<script>
  let readd = {
    updated: function () {
      console.log(this.x);
    }
  }
  let vm = new Vue({
    el: '#app',
    data() {
      return {
        x: 1
      }
    },
    methods: {
      add: function () {
        this.x++
      }
    },
    mixins: [readd]
  })
</script>

</html>
```

