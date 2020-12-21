# vue生命周期的理解

##### **beforeCreated阶段：**

vue实例的挂载元素el和数据对象data为undefined,还未初始化

##### created阶段：

vue实例的数据对象data有了，但是el还没有，不能进行DOM交互，需要$nextTick访问dom

##### beforeMount阶段：

vue实例的$el和data有了，但是挂载前为虚拟DOM，即将开始渲染，改变数据，不会触发updated

##### Mount阶段：

vue实例挂载完成，data.message渲染完毕，真实的DOM挂载完成，数据完成双向绑定，可以访问dom节点，通过$refs操作DOM

##### beforeUpdated阶段：

响应数据更新时调用，发生在虚拟DOM打补丁之前，可以在更新前访问现有的DOM，可以更改数据，不会造成重渲染

##### updated阶段：

虚拟DOM重新渲染和打补丁之后调用，组成新的DOM已经更新完成，不能在这个钩子函数里更改数据，防止死循环

##### beforeDestoryed阶段：

销毁前调用，vue实例还可以用，this可以获取实例，用于清除定时器，解绑事件

##### destoryed阶段

销毁后调用，所有事件监听器都会被移除，所有子实例都会被销毁