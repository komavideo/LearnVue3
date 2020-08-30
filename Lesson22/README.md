事件的多处理
==========

## 知识点

* 在事件接口中同时定义多个处理程序

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h2>点击次数：{{count}}</h2>
        <button class="btn btn-success m-2" @click="btnClick1(), btnClick2($event)">点它加1</button>
    </div>
    <script>
        const app = Vue.createApp({
            /* options */
            data() {
                return {
                    count: 0,
                }
            },
            methods: {
                btnClick1() {
                    this.count++;
                },
                btnClick2(event) {
                    console.log(event)
                    console.log(event.target)
                    console.log(event.target.attributes.class)
                    console.log(event.target.innerText)
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
