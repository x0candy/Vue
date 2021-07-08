**alias**

简单来说，就是给某个路径起一个别名，原路径与别名都会定向到一个地方

在根路径中，别名不起作用

```vue
<script>
import Vue from 'vue'
import Router from 'vue-router'
import HelloWorld from '@/components/HelloWorld'
import x0candy from '../components/x0candy.vue'
Vue.use(Router)

export default new Router({
  routes: [{
    path: '/',
    name: 'HelloWorld',
    component: HelloWorld
  },
  {
    path: '/hi',
    component: x0candy,
    alias: '/xyz'
  }
  ]
})
</script>

<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-link to="/hi">hi</router-link>
    <router-link to="/xyz">xyz</router-link>
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
</style>

```

