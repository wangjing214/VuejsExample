<!DOCTYPE html>
<html>
<head>
<title>组件+数组语法+绑定class</title>
<style>
    .haha{color:red;}
    .hehe{font-size: 100px}
</style>
</head>
<body>
<ul>
    <div id='app'>
    <li><h5>v-if条件渲染指定</h5></li>
    <ul>
        <li>
            <h5>key属性的存在，使得input元素不会被利用</h5>
        </li>
    </ul>
        <template v-if="type === 'name'">
            <label>用户名：</label>
            <input placeholder="输入名字" key="name-input">
        </template>
        <template v-else>
            <label>邮箱：</label>
            <input placeholder="输入邮箱" key="mail-input">
        </template>
        <button @click="c">切换输入类型</button>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                type: 'name'
            },
            methods: {
                c: function() {
                    this.type = this.type === 'name' ? 'mail' : 'name';
                }
            }
        })
        Vue.component('my-component', {
            template: '<p class="article">一此文本</p>'
        });
    </script>
</body>
</html>