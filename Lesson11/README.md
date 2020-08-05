模版语法 - 插值
=============

## Vue更新进度随时跟踪

https://github.com/vuejs/vue-next/releases

## 知识点

* 了解Vue模版语法中的插值语法

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h3>插值语法</h3>
        <span class="text-primary">{{ message }} </span>

        <hr>
        <h3>只渲染一次 - v-once</h3>
        <span v-once class="text-danger">{{ message }}</span>
        <br>
        <button class="btn btn-info" v-on:click="this.message='不要太悲观, 虽然上帝看不到。'">哦？</button>
        
        <hr>
        <h3>原始HTML - v-html</h3>
        {{ rawHtml }}
        <br>
        <span v-html="rawHtml"></span>
        
        <hr>
        <h3>绑定属性 - v-bind:xxx</h3>
        <button v-bind:disabled="isDisabledButton" v-on:click="this.isDisabledButton=true" class="btn btn-info">按我一下吧</button>
    </div>
    <script>
        Vue.createApp({/* options */
            data() {
                return {
                    message: '中国足球没戏了!',
                    rawHtml: '<b class=text-danger>恒大衰落了</b>',
                    isDisabledButton: false
                }
            },
        }).mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
