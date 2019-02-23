<!DOCTYPE html>
<html>
<head>
<title>v-show 改变元素的css属性display</title>
<style>
    .haha{color:red;}
    .hehe{font-size: 100px}
</style>
</head>
<body>
<ul>
    <div id='app'>
        <p v-show="status === 1">当status为 1 时显示该行</p>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                status: 1
            }
        })
    </script>
</body>
</html>