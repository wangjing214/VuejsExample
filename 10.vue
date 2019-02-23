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
    <li><h5>多个class并存</h5></li>
    </ul>
    <div id="app">
        <my-component :class="{ 'active':isActive }"></my-component>
        <div class="haha" :class="[{'active': isActive}, hehe]">dd</div>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                isActive: true,
                hehe: 'hehe'
            }
        })
        Vue.component('my-component', {
            template: '<p class="article">一此文本</p>'
        });
    </script>
</body>
</html>