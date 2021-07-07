**mount**

挂载扩展

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
  <div id="app"></div>
</body>

<script>
  let vm = Vue.extend({
    template: `<h1>mount</h1>`,
  })
  new vm().$mount('#app')
</script>

</html>
```

