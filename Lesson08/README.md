app.component自定义组件
======================

## 知识点

* 在单页App中定义自己的组件 - app.component

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <button class="btn btn-success" v-on:click="this.seen = !this.seen">万能按钮</button>
        <hr>
        <helo-world myname="koma" v-if="this.seen" />        
    </div>
    <script>
        const HelloVueApp = {
            data() {
                return {
                    seen: true,
                }
            },
        }
        const app = Vue.createApp(HelloVueApp)
        app.component('helo-world', {
            props: ['myname'],
            template: `<h1>helo {{ myname }}.</h1>`
        })
        app.mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
