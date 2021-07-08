**参数传递**

name直接传递参数 ,不推荐使用，下面讲用name作为标志来传递参数



用name作为标志，绑定to，在to中用params传递参数

```vue
<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-link to="/hi">hi</router-link>
    <router-link :to="{name:'name',params:{username:'x0candy'}}">name</router-link>
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<script>
//index.js
import Vue from 'vue'
import Router from 'vue-router'
import HelloWorld from '@/components/HelloWorld'
import x0candy from '../components/x0candy.vue'
import name from '../components/name.vue'
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
    children: [{
      path: 'name',
      name: 'name',
      component: name
    }]
  }
  ]
})

</script>
```



