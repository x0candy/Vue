**destroy**

卸载扩展

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
  <button onclick="des()">卸载</button>
</body>

<script>
  let vm = Vue.extend({
    template: `<h1>mount</h1>`,
  })
  let app = new vm().$mount('#app')

  function des() {
    app.$destroy()
    console.log('卸载');
  }
</script>

</html>
```

