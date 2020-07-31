v-for循环一个数组
================

## 知识点

* 使用v-for循环一个数组

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <button class="btn btn-success" v-on:click="this.seen = !this.seen">今天的预定</button>
        <hr>
        <ol>
            <li v-for="todo in todos" v-if="seen">
                {{ todo.text }}
            </li>
        </ol>
    </div>
    <script>
        const HelloVueApp = {
            data() {
                return {
                    seen: false,
                    todos: [
                        { text: '吃饭' },
                        { text: '睡觉' },
                        { text: '打游戏' }
                    ]
                }
            },
        }
        Vue.createApp(HelloVueApp).mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
