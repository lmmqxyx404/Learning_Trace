# vue react和原生H5开发的不同
原生更有利于做SEO,方便被搜索引擎收录

# 大型项目中的数据流
子组件的数据可以在父组件创建的时候进行请求与加载

特别是子组件初始设置为false的情况下，可以让用户无感知加载

带来的编码问题就是，子组件请求数据的方法，在父组件中重写。

并且在父组件中请求好后，先赋值给子组件同名变量，父组件也设置一个同名变量

之后通过ref的方式传递给子组件。子组件加载好方法

## 父子数据传递
在不引入vuex 时，可以考虑三种方案
1. $emit and $on
最基本的使用

2. provide and inject
方便在祖先与后代节点之间传递

3. $parent and $child
注意父组件的层级问题

# Debug 
## 项目崩溃的解决思路
可以在package.json文件中，按照如下方法设置serve属性，可以解决前端大型项目中内存溢出问题,不同框架解决思路大同小异。具体可以搜索一下
"serve": "node --max_old_space_size=4096 node_modules/@vue/cli-service/bin/vue-cli-service.js serve ",
上述代码从docx中粘贴时，可能会出现未知错误
``` FATAL ERROR: Ineffective mark-compacts near heap limit Allocation failed - JavaScript heap out of memory ```

## 当生命周期函数没有执行的时候，切记要记得检查大括号的位置

## 注意组件嵌套的时候，记得定时清空缓存，刷新浏览器，重新获取数据

## 当页面卡死的时候，注意查看是否有网络请求，再来判断是前端问题还是后端问题

## Object.prototype.toString.call() 判断变量类型的唯一推荐的正确方法

## 后端返回的数据不是总是可靠的，实际开发中要考虑兼容性

# Vue 语法特性
## SFC single file component

## 可以为行为绑定动态事件
比如说，单击响应A，或者双击响应A
## 注意常见的事件修饰符含义 stop prevent

## 补充指令
### v-once 只需要渲染一次
### v-memo 作用不大

## 虚拟 DOM 原理
### 生成抽象语法树（AST）
# vue 中操作DOM的方式 (2.x)
1. 直接使用原生DOM对象
2. 使用jQuery语法
3. 使用 ```$ref```

# Vue + TypeScript 开发 OA 系统(Office Automation) 

# 开发中碰到 不断的 sockjs-node/info?t=1554978**** 网络请求错误，注意可能是代理软件接受了相应的网络请求，关闭代理即可

# VUE中的一些配置文件
## 1. 记得可以禁用eslint 配置文件，编写.prettierc文件进行代码格式化
## 2. The tsconfig.json file is indispensable when use TypeScript
## 3. 查看vue/cli网站关于.env相关文件的配置
## 4. TypeScript 中接口和api暴露方式可以统一用一个文件夹来表示

# 在uniapp中使用Vue 
## 1. 这个框架中有个特殊的原生类型nvue(native vue)
## 2. pages.json文件中设置 tabBar 值时，注意pagePath，必须与pages中的path完全一致
## 3. uniapp 中image标签与标准(img)的是不一致的

# Vuex
## 1. mutation 是用来处理同步的请求的，action是用来处理异步请求的。state最好与computed一一对应。
## 2. state中的某个属性是对象时，注意该对象中的属性值发生变化时，不会触发getters。
### 2.1 因此要更新state中某个key，key对应的数据类型不是基本类型(primitive type)，要使用Vue.set().
Vue.set() 很多时候等价于 this.$nextTick(), 注意使用Vue.set()，会触发 watch。
### demo
```
state:{
  attr:{
    id:2
  }
}
```
当id发生变化时，依赖它的getters不会发生变化。因此在特定业务场景下，可以考虑属性用basic value。
# Vue-Router
## 1. VueRouter 重点了解掌握编程式路由还有路由传递参数
### 路由传参时，注意在注册路由时，是否要保留相关路径接收相关参数
``` /:id ``` 这种情况下必须接收参数
## 2. VueRouter 中的导航守卫与axios(ajax)中的请求/响应拦截器是不一样的

# VUE3 + TS
VUE3 supports ts more friendly.
vue-global-api 
a useful plugin

## Vue3 特性
### ref isRef shallowRef
```ref``` 使用 proxy 劫持对象，实现深层次响应式更新
```isRef``` 检测对象是否被 ref 包裹
```shallowRef``` 一般用于保护第三方库对象
```ref shallowRef``` 一般不能一起修改，否则会引起shallowRef更新

### triggerRef customRef
triggerRef 强制更新收集到的依赖  类似于```Vue.$set()```

### lifecycle
#### different lifecycles
|||
|--|--|
|directive|多了两个生命周期|
|keep-alive|  多了两个独特的生命周期  |

### 响应式对象与普通对象
#### vue3 中的响应式对象
会被```reactive() ``` 或者```ref() ```调用，如果想恢复成普通对象，调用toRaw即可
普通对象中的某个属性变为响应式，只需要使用```toRef()```。
如果是多个，使用 ```toRefs()```即可


# vue.config.js
## 前端设置代理，解决跨域类似问题后，注意要重新启动整个项目，否则请求地址不生效。 相应的也需要后端配合，查看是否有前端请求。尽量避免此类防呆问题
## devServer
关于设置代理，必须明确，代理只有在本地开发时才需要。部署到线上，也就是生产环境时，是不需要的。因此必须注意环境变量在.env文件中的设置
此外 代理设置  部署到线上时，要与nginx相配合
