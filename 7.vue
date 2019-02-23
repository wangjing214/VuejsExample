<!DOCTYPE html>
<html>
<head>
<title>未跑通v-bind</title>
</head>
<body>
    <ul>
    <li><h5>v-bind 是动态更新HTML元素上的属性</h5></li>
    </ul>
    <div id="app">
        <a :href="url2">aa <a/>
        <img :src="imagUrl">
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                url2: 'http://baidu.com',
                imgUrl: 'http://image.baidu.com'
            }
        })
    </script>
</body>
</html>