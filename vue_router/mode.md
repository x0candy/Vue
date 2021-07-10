**mode**

主要讲mode与404页面的处理

```vue
<script>
import Vue from 'vue'
import Router from 'vue-router'
import HelloWorld from '@/components/HelloWorld'
import x0candy from '../components/x0candy.vue'
import hi from '../components/hi.vue'
import Error from '../components/404.vue'
Vue.use(Router)

export default new Router({
  mode: 'history',      //有history与hash，history就是正常的url，hash看起来像无意义的字符排列
  routes: [{
    path: '/',
    name: 'HelloWorld',
    component: HelloWorld
  },
  {
    path: '/hi',
    component: x0candy,
    alias: '/xyz'
  },
  {
    path: '/hh',
    component: hi
  },
  {                                   //404页面处理
    path: '*',
    component: Error
  }
  ]
})
</script>
```

