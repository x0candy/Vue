**propsData**

propsData用在全局扩展传递数据

1. 在全局扩展中加入props接收数据
2. 在实例化时用propsData传递数据
3. 用插值表达式写入模板

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
    
  </div>
</body>

<script>
  var  header_a = Vue.extend({
    template:`<p>{{message}}-{{a}}</p>`,
    data:function(){
        return {
            message:'Hello,I am Header'
        }
    },
    props:['a']
}); 
new header_a({propsData:{a:1}}).$mount('#app');
</script>

</html>
```

