**初识vuex**

vuex，状态管理工具，数据仓库

在一些项目中，有些数据是共享的，如果每一次都去请求，那么请求次数可能会很多

我们可以请求一次，然后将数据存储在vuex中

```vue
<script>
import Vue from 'vue'
import Vuex from 'vuex'
Vue.use(Vuex)
const state = {
  count: 1
}
const mutations = {
  add (state) {
    state.count++
  },
  reduce (state) {
    state.count--
  }
}
export default new Vuex.Store({
  state,
  mutations
})
</script>
```

