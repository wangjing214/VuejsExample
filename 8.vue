<!DOCTYPE html>
<html>
<head>
<title>绑定class的几种方式</title>
<style>.haha{color:red;}</style>
</head>
<body>
<ul>
    <li><h5>多个class并存</h5></li>
    </ul>
    <div id="app">
        <div class="haha" :class="{'active': isActive}">dd</div>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                isActive: true
            }
        })
    </script>
</body>
</html>