**state**

状态对象，简单来说就是存储的数据



三种方式使用state：

$store

计算属性

mapState与计算属性

```vue
<template>
  <div>
    <h1>{{$store.state.count}}--{{count}}</h1>
    <button @click="$store.commit('add')">+</button>
    <button @click="$store.commit('reduce')">-</button>
  </div>
</template>

<script>
import store from '../vuex/store'
import { mapState } from 'vuex'
export default {
  name: 'counter',
  data () {
    return {
      msg: 'hello world'
    }
  },
  computed: mapState({              //可以简写为computed:mapState(['count'])
    count: state => state.count
  }),
  store
}
</script>

<style scoped>
</style>

```

