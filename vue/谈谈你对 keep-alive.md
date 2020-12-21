### 谈谈你对 keep-alive

keep-alive 是 Vue 内置的一个组件，可以使`被包含的组件保留状态`，`避免重新渲染` ，其有以下特性：

采用LRU算法

- 一般结合路由和动态组件一起使用，用于缓存组件；
- 提供 `include` 和 `exclude` 属性，两者都支持字符串或正则表达式， include 表示`只有名称匹配`的组件`会被缓存`，exclude 表示任何名称匹配的组件都`不会被缓存` ，其中 exclude 的`优先级`比 include 高；
- 对应两个钩子函数 `activated` 和 `deactivated` ，当组件被激活时，触发钩子函数 activated，当组件被移除时，触发钩子函数 deactivated。允许组件有条件的进行缓存

**keep-alive的生命周期**，用来得知当前组件是否处于活跃状态

1. *activated：* 页面第一次进入的时候，钩子触发的顺序是created->mounted->activated
2. *deactivated:* 页面退出的时候会触发deactivated，当再次前进或者后退的时候只触发activated

