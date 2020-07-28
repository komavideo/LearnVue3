v-bind绑定数据
=============

## 知识点

* 使用v-bind属性绑定数据

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <div v-bind:title="message">
            走开，别把手放上来。
        </div>
    </div>    
    <script>
        const HelloVueApp = {
            data() {
                return {
                    message: '你好坏!!'
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
