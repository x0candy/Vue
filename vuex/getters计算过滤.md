**getters**

有点像computed

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
import { mapState, mapMutations, mapGetters } from 'vuex'
export default {
  name: 'counter',
  data () {
    return {
      msg: 'hello world'
    }
  },
  computed: {
    ...mapState(['count']),
    ...mapGetters(['count'])
  },
  store,
  methods: mapMutations(['add', 'reduce'])
}
</script>

<style scoped>
</style>

```



