<!DOCTYPE html>
<html>
<head>
<title>++1 ++2 单击数</title>
<style>
    [v-cloak] {display:none !important;}
</style>
</head>
<body>
    <div id='app' v-cloak>
        点击次数： {{ counter }}
        <button @click="counter+=2">+2</button>
        点击次数： {{ counter2 }}
        <button @click="handleAdd()">+1</button>
        <button @click="handleAdd(10)">+10</button>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                counter: 0,
                counter2: 0
            },
            methods: {
                handleAdd: function (num) {
                    num = num || 1;
                    this.counter2 += num;
                }
            }
        })
    </script>
</body>
</html>