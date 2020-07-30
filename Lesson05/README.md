v-model双向绑定
==============

## 知识点

* 使用v-model实现变量的双向绑定

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <p>{{ message }}</p>
        <input class="form-control" v-model="message" />
    </div>
    <script>
        const HelloVueApp = {
            data() {
                return {
                    message: '我爱NBA!!'
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
