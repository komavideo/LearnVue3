事件修饰符
==========

## 知识点

* .prevent -> event.preventDefault()
* .stop -> event.stopPropagation()
* .capture
* .self
* .once
* .passive

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h2>表单演示(阻止提交)</h2>
        <!-- <form @submit.prevent="noSubmit"> -->
        <form>
            <label for="new-todo">添加预定：</label>
            <input v-model="newTodoText" id="new-todo" placeholder="例:一起吃鸡" />
            <button @click="btnAddTodo()">添加</button>
            <ul>
                <li v-for="todo in todos">{{todo}}</li>
            </ul>
        </form>
    </div>
    <script>
        const app = Vue.createApp({
            /* options */
            data() {
                return {
                    newTodoText: '',
                    todos: []
                }
            },
            methods: {
                btnAddTodo() {
                    if (event) {
                        // 阻止事件发生
                        event.preventDefault()
                    }
                    this.todos.push(this.newTodoText)
                    this.newTodoText = ""
                },
                noSubmit() {
                    console.log("noSubmit")
                }
            }
        })
        app.mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
