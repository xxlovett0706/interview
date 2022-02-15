# Vue

Vue data() 问什么这么设计

他是一个闭包的设计，为了保证每一个组件拥有一个私有空间

## MVC 和 MVVM

MVC 是 Model View Controller

通过 Controller 来控制 View

MVVM 是 Model View ViewModel

通过 ViewModel 数据驱动 View

## v-model 双向数据绑定

通过 事件监听和Object.defineProperty()
set赋值需要配合私有数据

## v-if 和 v-show

v-if 满足条件才渲染dom 应用场景 单次判断

v-show 是隐藏 应用场景 多次切换；不能用于权限操作

## 虚拟dom

虚拟dom是什么
1. 出现在Vue2.x版本
2. 本质就是一个 js对象

虚拟dom在Vue中做了什么
1. 将真实Dom转化为虚拟Dom也就是js对象
2. 在更新的时候做对比

虚拟Dom如何提升vue的渲染效率
1. 局部更新（Dom）

## diff 算法中的patch以及update

patch:根据js对象（虚拟Dom）创建真实Dom；再添加相应的属性以及利用递归添加子Dom。
update: 对比新老vnode，然后利用递归和替换实现局部更新

## Vue的两大核心

数据驱动；组件化

## Vue 响应式原理

发布订阅模式 + 数据劫持

