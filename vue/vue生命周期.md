生命周期：创建、初始化、挂载、更新、销毁
beforeCreate：此时节点没有创建，data和methods属性没有初始化好
created：此时组件的data和methods已经创建ok,未开始编译模板（template），一般在created中进行调用接口操作、如获取渲染表格中的数据
路由传参的参数，通过id或ref获取标签属性，可以通过this.$nextTick回调中进行
beforeMounted：模板编译完成，未渲染到页面上，可进行的操作与create相似
mounted：挂载完成、能正常获取dom节点
beforeUpdate：在更新之前执行此函数，此时data中的状态已经是最新的了，页面没有渲染上去，效果未展示
updated：得到最新的状态，页面也得到最新的状态。updated用法与comptued和watch相似，能通过数据变化来判断起到监听的作用。比如在updated中监听指定password进行操作
beforeDestroy：在组件销毁之前调用，在这一步。仍然完全可用
destroyed：vue实例销毁后调用，调用后，vue实例指示的所有的东西都会解绑定，所有的事件监听器会被移除，所有的实例也会被销毁
activated；只在使用keep-alive标签中使用，每次进入都会执行钩子中的函数，只在组件刚创建时创建
deactivated：在切换组件时触发