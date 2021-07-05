**methods**

methods中方法的传值

.native修饰调用原生方法

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
    <h1>{{num}}</h1>
    <button @click="add(1)">+1</button>
    <btn @click.native="add(2)"></btn>
    <!--.native为使用原生方法-->
  </div>
</body>

<script>
  let app = Vue.component('btn', {
    template: `<button>+2</button>`
  })
  new Vue({
    el: '#app',
    data: {
      num: 1
    },
    methods: {
      add: function (num) {
        this.num += num
      }
    }
  })
</script>

</html><!DOCTYPE html>
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
    <h1>{{num}}</h1>
    <button @click="add(1)">+1</button>
    <btn @click.native="add(2)"></btn>
    <!--.native为使用原生方法-->
  </div>
</body>

<script>
  let app = Vue.component('btn', {
    template: `<button>+2</button>`
  })
  new Vue({
    el: '#app',
    data: {
      num: 1
    },
    methods: {
      add: function (num) {
        this.num += num
      }
    }
  })
</script>

</html><!DOCTYPE html>
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
    <h1>{{num}}</h1>
    <button @click="add(1)">+1</button>
    <btn @click.native="add(2)"></btn>
    <!--.native为使用原生方法-->
  </div>
</body>

<script>
  let app = Vue.component('btn', {
    template: `<button>+2</button>`
  })
  new Vue({
    el: '#app',
    data: {
      num: 1
    },
    methods: {
      add: function (num) {
        this.num += num
      }
    }
  })
</script>

</html>
```



