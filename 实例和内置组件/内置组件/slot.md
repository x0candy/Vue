**slot(插槽)**

官方解释：

插槽（Slot）是Vue提出来的一个概念，正如名字一样，插槽用于决定将所携带的内容，插入到指定的某个位置，从而使模板分块，具有模块化的特质和更大的重用性。插槽显不显示、怎样显示是由父组件来控制的，而插槽在哪里显示就由子组件来进行控制

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
    <mob>
      <span slot="pname">{{people.name}}</span>
      <span slot="page">{{people.age}}</span>
      <span slot="pwork">{{people.work}}</span>
    </mob>
  </div>
</body>

<template id="mob">
  <div>
    <p>name: <slot name="pname"></slot></p>
    <p>age: <slot name="page"></slot></p>
    <p>work: <slot name="pwork"></slot></p>
  </div>
</template>

<script>
  let mob = {
    template: '#mob'
  }
  let app = new Vue({
    el: '#app',
    data: {
      people: {
        name: 'asd',
        age: 18,
        work: 'web'
      }
    },
    components: {
      "mob": mob
    }
  })
</script>

</html>
```

