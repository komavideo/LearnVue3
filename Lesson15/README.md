计算属性与函数的区别
=================

## 知识点

* 组件模版脚本中计算属性与函数的区别

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h2>{{ msg }} / {{ this.getResult() }}</h2>
        <h3>result: {{this.result}} / {{ this.getDateTime() }}</h3>
        <button @click="btnClick()" class="btn btn-success">一个按钮</button>
    </div>
    <script>
        Vue.createApp({
            /* options */
            data() {
                return {
                    msg: "i love u."
                }
            },
            computed: {
                result() {
                    // return this.msg
                    return this.getDateTime()
                }
            },
            methods: {
                getResult() {
                    return this.msg
                },
                getDateTime() {
                    now = new Date()
                    return "00:" + now.getMinutes() + ":" + now.getSeconds()
                },
                btnClick() {
                    console.log("this.result:", this.result)
                    console.log("this.getDateTime():", this.getDateTime())
                }
            }
        }).mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
