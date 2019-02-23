<!DOCTYPE html>
<html>
<head></head>
<body>
    <div id="app">
        <ul>
            <li v-for="book in books">{{ book.name }}</li>
        </ul>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        new Vue({
            el: '#app', 
            data: {
                books: [
                    { name: '<Vue.js实战>' },
                    { name: '<JavaScript语言精粹>' },
                    { name: '<javascript 高级程序设计>' }
                ]
            }
        })
    </script>
</body>
</html>