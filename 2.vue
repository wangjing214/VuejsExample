<!DOCTYPE html>
<html>
<head>
    <title>数据绑定</title>
</head>
<body>
<h4>在input标签上，有一个v-model的指令，它的值对应于我们创建的Vue实例的data选项中的name字段，这就是Vue的数据绑定</h4>
    <div id="app">
        <input type="text" v-model="name" placebolder="你的名字">
        <h1>你好，{{ name }}</h1>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        new Vue({
            el: '#app',
            data: {
                name: ''
            }
        })
    </script>
</body>
</html>