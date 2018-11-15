# vue-optimize
vue前端优化
## 使用require-ensure来加载路由组件
```
const Home = r =>require.ensure([依赖的模块数组],回调函数，模块名),最后一个是chunk名，具有相同名字的会打包到同一个js文件中
例如：
const Home =r=>  require([],()=>r(require('@/components/home.vue')),‘Home’)
```
