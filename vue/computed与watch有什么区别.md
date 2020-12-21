# computed与watch有什么区别

##### computed

```js
computed有缓存，有属性依赖，只有当属性依赖发生变化，
它才会在下次重新计算
使用场景购物车计算
```

##### watch

```
多用于监听事件，动态的监听数据，当监听的数据发生变化，
watch会产生两个值，newValue和OldValue,
用于监听数据变化，其中可以监听的数据来源有三部分：props、data、computed内的数据；
watch提供两个参数（newValue，oldValue），第一个参数是新值，第二个参数保存旧值；
它是个异步，无依赖

当一条数据影响多条数据的时候         搜索数据
执行异步或开销较大的操作时，使用watch 
```

