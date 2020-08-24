v-for综合例
==========

## Vue更新进度随时跟踪

https://github.com/vuejs/vue-next/releases

## 知识点

* 结合form,event,v-for的一个综合的例子

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <form v-on:submit.prevent="addNewTodo">
            <label for="new-todo">添加预定：</label>
            <input v-model="newTodoText" id="new-todo" placeholder="例:一起吃鸡" />
            <button>添加</button>
        </form>
        <hr/>
        <ul class="p-3">
            <todo-item v-for="(todo, index) in todos" :key="todo.id" :title="todo.title"
                @remove="todos.splice(index, 1)"></todo-item>
        </ul>
    </div>
    <script>
        const app = Vue.createApp({
            /* options */
            data() {
                return {
                    newTodoText: '',
                    todos: [{
                            id: 1,
                            title: '给女友买礼物'
                        },
                        {
                            id: 2,
                            title: '请女友吃大餐'
                        },
                        {
                            id: 3,
                            title: '陪女友看电影'
                        }
                    ],
                    nextTodoId: 4
                }
            },
            methods: {
                addNewTodo() {
                    this.todos.push({
                        id: this.nextTodoId++,
                        title: this.newTodoText
                    })
                    this.newTodoText = ''
                }
            }
        })

        app.component('todo-item', {
            template: `
                <li class='p-2'>
                {{ title }}
                <button @click="$emit('remove')">删除</button>
                </li>
            `,
            props: ['title']
        })

        app.mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
