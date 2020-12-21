# v-model的原理

用于表单数据的双向绑定

- v-bind:绑定响应式数据
- 触发oninput 事件并传递数据
- 通过oninput触发事件获取当前$event.target.value，然后赋值给当前变量。







v-model主要提供了两个功能，view层输入值影zhi响data的属性值，data属性值发生改dao变会更新view层的数值变化。
其核心就是，一方面modal层通过defineProperty来劫持每个属性，一旦监听到变化通过相关的页面元素更新。另一方面通过编译模板文件，为控件的v-model绑定input事件，从而页面输入能实时更新相关data属性值。