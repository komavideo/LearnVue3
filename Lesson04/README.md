v-on实现事件处理
==============

## Vue更新进度随时跟踪

https://github.com/vuejs/vue-next/releases

## 知识点

* 使用v-on指令绑定一个click事件

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h3>{{ message }}</h3>
        <button class="btn btn-success" v-on:click="reverseMessage">反转字符串</button>
    </div>
    <script>
        const HelloVueApp = {
            data() {
                return {
                    message: '我爱NBA!!'
                }
            },
            methods: {
                reverseMessage() {
                    this.message = this.message
                        .split('')
                        .reverse()
                        .join('')
                }
            }
        }
        Vue.createApp(HelloVueApp).mount('#hello-vue')
    </script>    
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
