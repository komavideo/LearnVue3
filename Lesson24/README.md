按键修饰符
==========

## 知识点

* Vue中侦听键盘事件的方法

### 最常用的按键

+ .enter
+ .tab
+ .delete (同时捕获“删除”和“退格”键)
+ .esc
+ .space
+ .up
+ .down
+ .left
+ .right

### 系统按键

+ .ctrl
+ .alt
+ .shift
+ .meta (Mac Command)

### 键盘按键一览

https://developer.mozilla.org/en-US/docs/Web/API/KeyboardEvent/key/Key_Values

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h2>表单演示(阻止提交)</h2>
        <form @submit.prevent>
            <label for="new-todo">添加预定：</label>
            <input v-model="newTodoText" id="new-todo" placeholder="例:一起吃鸡" @keyup.enter="btnAddTodo()" />
            <button @click.ctrl="btnAddTodo()">添加(按住Ctrl键)</button>
            <button @click.right="btnAddTodo()">添加(接收鼠标右键点击))</button>
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
                    if (this.newTodoText.length > 0) {
                        this.todos.push(this.newTodoText)
                        this.newTodoText = ""
                    }
                },
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
