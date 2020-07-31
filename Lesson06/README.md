v-if控制显示条件
==============

## 知识点

* 应用v-if控制元素的显示

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <p>
            <button class="btn btn-success" v-on:click="this.seen = !this.seen">设定按钮</button>
        </p>
        <div v-if="seen">能看见我吗？</div>
    </div>
    <script>
        const HelloVueApp = {
            data() {
                return {
                    seen: true
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
