<!DOCTYPE html>
<html>
<head>
    <title>常见沟子</title>
</head>
<body>
<h4>常见沟子：</h4>
<ul>
<li><h5>created- 创建完实例后调用，完成数据观测，尚未挂载，$el还不可用</h5></li>
<li><h5>mounted- el挂载到实例上后调用，一般我们的第一个业务逻辑会在这里开始</h5></li>
<li><h5>beforeDestroy- 实例销毁之前调用，主要解绑一些使用addEventListener监听的事件等</h5></li>
</ul>
    <div id="app">
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        new Vue({
            el: '#app',
            data: {
                a: 2
            },
            created: function () {
                console.log(this.a);// 2
            },
            mounted: function () {
                console.log(this.$el);// <div id="app"></div>
            }
        })
    </script>
</body>
</html>