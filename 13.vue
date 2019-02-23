<!DOCTYPE html>
<html>
<head>
<title>v-for 列表渲染指令</title>
<style>
    .haha{color:red;}
    .hehe{font-size: 100px}
    [v-cloak] {display:none !important;}
</style>
</head>
<body>
    <ul>
        <li>
            <h5>vuejs文件还没加载完成时，页面上会闪动下{{book.name}}，是因为vue创建实例、编译模板时Dom才会被替换，[v-cloak] {display:none !important;}这句Css就是解决一闪的问题</h5>
        </li>
    </ul>
    <div id='app' v-cloak>
        <span ></span>
        <ul>
            <li v-for="book in books">{{ book.name }}</li>
        </ul>
        <hr>
        <ul>
            <li v-for="(book, index) in books">{{ index }} -- {{ book.name }}</li>
        </ul>
        <hr>
        <ul>
            <li v-for="(value, key, index) in user">{{ index }} -- {{ key }} -- {{ value }}</li>
        </ul>
        <hr>
        <span v-for="n in 10"> {{ n }} </span>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                books: [
                    {name: 'book 111', age: 11},
                    {name: 'book 2222', age: 22},
                    {name: 'book 33333', age: 33}
                ],
                user: {
                    name: 'wj',
                    gender: '男',
                    age: 16
                }
            }
        })
    </script>
</body>
</html>