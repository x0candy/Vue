**actions**

actions使用mutations中的方法修改state

actions支持异步操作，mutations只能同步

```vue
<script>
//store.js
const actions = {
  change (context) {
    context.commit('add')
    setTimeout(() => {
      console.log(2)
    }, 3000)
    console.log(1)
  }
}

//组件中引入
methods: {
    ...mapMutations(['add', 'reduce']),
    ...mapActions(['change'])
}
</script>
```

