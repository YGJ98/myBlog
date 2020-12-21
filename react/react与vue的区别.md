##### react与vue的区别

1.vue使用的是template模版编写。react使用的是jsx语法。

2.状态管理：react中的状态全部存入state中，通常修改的时候需要用到setState方法来更新状态。 vue中的state对象不是必须，vue是通过data属性在vue对象中进行管理

3.监听数据的变化，vue劫持一些函数，能精确的知道数据变化。react中默认是通过比较引用的方式去进行，如果不优化使用shouldComponentUpdate/PureComponent方法优化，那会导致大量的虚拟dom重新渲染

4.数据流不同：vue可以进行组件与dom之间v-modle双向绑定。react从始至终都只有单向数据流

5.vue中使用的是mixins。react使用的是Hoc高阶组件