# v-show与v-if的区别

共同点： 都能控制元素的显示和隐藏

不同点：

v-show是通过控制css中的display设置为none,控制元素的隐藏，只编译一次；

v-if是动态的向DOM树内添加或删除DOM元素，若初始值为false，就不编译了，而且v-if是不断的销毁和创建，比较消耗性能

总结： 如果要频繁的切换某个节点，使用v-show（切换开销比较小，初始开销较大）

如果不需要频繁切换某个节点使用v-if(初始渲染开销较小，切换开销较大)