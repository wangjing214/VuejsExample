<!DOCTYPE html>
<html>
<head>
    <title>插值与表达式 2</title>
</head>
<body>
<h4>插值与表达式：</h4>
<ul>
<li><h5>使用双大括号(Mustache 语法)“{{}}”是最基本的文本插值方法，它会自动将我们双向绑定的数据实时显示出来</h5></li>
<li><h5>v-html 输出HTML，而不是将数据解释后的纯文本</h5></li>
<li><h5>v-html 缺点是，易造成XSS攻击，需要服务端对用户提交的内容进行处理</h5></li>
<li><h5>v-pre  想显示{{}}，而不进行替换</h5></li>
<li><h5>{{ }} 除简单绑定值外，还要以使用javascript表达式进行简单运算、三元运算等</h5></li>
<li><h5>Vue.js只支持单个表达式，不支持语句的流控制。另外，在表达式中不能使用用户自定义全局变量，只能使用Vue白名单内的全司变量，
例如 Math 和 Date。</h5></li>
<li>
<ul>
<li><h5>这是语句，不是表达式：{{ var book = 'Vue.js实战' }}</h5></li>
<li><h5>不能使用流控制，要使用三元运算：{{ if (ok) return msg }}</h5></li>
</ul>
</li>
</ul>
    <div id="app">
        <div>
            <span v-html="link"></span>
        <div>
        <div>
            {{ link2 }}
        </div>
        <div>
            {{ number / 10 }}
        </div>
        <div>
            {{ isOk ? '确定' : '取消' }}
        </div>
        <!--<div>
            {{ text2.split(',').reverse(),join(',') }}
        </div>-->
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        new Vue({
            el: '#app',
            data: {
                link: '<a href="#">这是一个连接</a>',
                link2: '<a href="#">这是一个连接</a>',
                number: 100,
                isOk: false,
                //text2: '123,456'// 456,123
            }
        })
    </script>
</body>
</html>