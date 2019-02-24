<!DOCTYPE html>
<html>
<head>
<title>filter 数组更新</title>
<style>
    [v-cloak] {display:none !important;}
</style>
</head>
<body>
    <div id='app' v-cloak>
        <ul>
            <template v-for="book in books">
                <li>书名：{{ book.name }}</li>
                <li>作者：{{ book.author }}</li>
            </template>
        </ul>
    </div>
    <script src="https://unpkg.com/vue/dist/vue.min.js"></script>
    <script>
        var app = new Vue({
            el: '#app',
            data: {
                books: [
                    {
                        name: 'book 111',
                        author: 'wj'
                    },
                    {
                        name: 'book 22',
                        author: 'wj22'
                    },
                    {
                        name: 'haha 33',
                        author: 'wj33'
                    },
                ]
            }
        })

        app.books = app.books.filter (function(item) {
            return item.name.match(/book/);
        });
    </script>
</body>
</html>