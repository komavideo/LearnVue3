事件处理
==========

## Vue更新进度随时跟踪

https://github.com/vuejs/vue-next/releases

## 知识点

* Vue中事件的处理方法

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h2>点击次数：{{count}}</h2>
        <button class="btn btn-success m-2" @click="btnClick1()">点它1</button>
        <button class="btn btn-info m-2" @click="btnClick2($event)">点它2</button>
        <hr>
        <h2>表单演示(阻止提交)</h2>
        <form>
            <label for="new-todo">添加预定：</label>
            <input v-model="newTodoText" id="new-todo" placeholder="例:一起吃鸡" />
            <button @click="btnClick3($event)">添加</button>
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
                    count: 0,
                    newTodoText: '',
                    todos: []
                }
            },
            methods: {
                btnClick1() {
                    this.count++;
                },
                btnClick2(event) {
                    this.count++;
                    console.log(event)
                    console.log(event.target)
                    console.log(event.target.attributes.class)
                    console.log(event.target.innerText)
                },
                btnClick3(event) {
                    // if (event) {
                    //     // 阻止事件发生
                    //     event.preventDefault()
                    // }
                    this.todos.push(this.newTodoText)
                    this.newTodoText = ""
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
