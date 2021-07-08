**url传参**

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
    path: '/hi/:Id/:Title',             //用冒号
    component: x0candy
  }
  ]
})

</script>

<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-link to="/hi/999/asdadsa">hi</router-link>   <!--参数传递-->
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

