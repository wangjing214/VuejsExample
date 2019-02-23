<!DOCTYPE html>
<html>
<head>
    <title>插值与表达式</title>
</head>
<body>
<h4>插值与表达式：</h4>
<ul>
<li><h5>使用双大括号(Mustache 语法)“{{}}”是最基本的文本插值方法，它会自动将我们双向绑定的数据实时显示出来</h5></li>
</ul>
    <div id="app">
        {{ book }}
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        new Vue({
            el: '#app',
            data: {
                book: '<Vue.js实战>'
            }
        })
    </script>
</body>
</html>