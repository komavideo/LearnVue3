计算属性(setter)
===============

## 知识点

* Vue 3中的计算属性之setter

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h3>{{this.x}} + {{this.y}} = {{this.result}}</h3>
        <button @click="this.result=100" class="btn btn-success">重新设定 x, y</button>
    </div>
    <script>
        Vue.createApp({/* options */
            data() {
                return {
                    x: 10,
                    y: 20
                }
            },
            computed: {
                result: {
                    // getter
                    get() {
                        return this.x + this.y
                    },
                    // setter
                    set(newValue) {
                        this.x = newValue / 2
                        this.y = newValue / 2
                    }
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
