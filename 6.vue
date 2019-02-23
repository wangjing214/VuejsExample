<!DOCTYPE html>
<html>
<head>
    <title>过滤器</title>
</head>
<body>
<h4>过滤器：</h4>
<ul>
<li><h5>Vue.js支持在{{}}插值的尾部添加一个管道符“（|）”对数进行过滤</h5></li>
<li><h5>管道常用于格式化文本，比如字母全部大写</h5></li>
<li><h5>过滤器应当用于处理简单的文本转换，如果要实现更为复杂的数据变换，应该使用计算属性</h5></li>
</ul>
    <div id="app">
        <div>
            {{ date | formatDate }}
        <div>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        // 在月分、日期、小时等小于10时前面补0
        var padDate = function(value) {
            return value < 10 ? '0' + value : value;
        };
        var app = new Vue({
            el: '#app',
            data: {
                date: new Date()
            },
            mounted: function () {
                var _this = this; //声明一个变量指向Vue实例this，保证作用域一致
                this.timer = setInterval(function() {
                    _this.date = new Date(); //修改数据date
                });
            },
            filters: {
                formatDate: function(value) {
                    var date = new Date(value);
                    var year = date.getFullYear();
                    var month = padDate(date.getMonth() + 1);
                    var day = padDate(date.getDate());
                    var hours = padDate(date.getHours())
                    var minutes = padDate(date.getMinutes());
                    var seconds = padDate(date.getSeconds());
                    return year + '-' + month + '-' + day + ' ' + hours + ':' + minutes + ':' + seconds;
                }
            },
            beforeDestroy: function() {
                if (this.timer) {
                    clearInterval(this.timer); //在Vue实例销毁前，清楚定时器
                }
            }
        })
    </script>
</body>
</html>