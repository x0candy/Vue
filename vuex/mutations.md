**mutations**

改变状态的一些方法

```vue
<template>
  <div>
    <h1>{{$store.state.count}}--{{count}}</h1>
    <button @click="$store.commit('add',10)">+</button>  <!--commit触发，10为传递的参数-->
    <button @click="$store.commit('reduce')">-</button>
  </div>
</template>

<script>
import store from '../vuex/store'
import { mapState, mapMutations } from 'vuex'
export default {
  name: 'counter',
  data () {
    return {
      msg: 'hello world'
    }
  },
  computed: mapState(['count']),
  store,
  methods: mapMutations(['add', 'reduce'])           //简写形式
}
</script>

<style scoped>
</style>

```

