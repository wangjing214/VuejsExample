<!DOCTYPE html>
<html>
<head>
<title>数组语法绑定class</title>
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
    </script>
</body>
</html>