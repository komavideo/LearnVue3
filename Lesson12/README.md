简化v-bind和v-on
================

## 知识点

* 简化属性绑定：v-bind -> :attr
* 简化事件绑定：v-on -> @event

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h3>属性绑定</h3>
        <!-- 完整写法：v-bind:href -->
        <a v-bind:href="komavideo" class="link" target="_blank">小马视频</a><br />
        <!-- 省略写法：:href -->
        <a :href="komavideo" class="link" target="_blank">小马视频</a>
        <h3>事件绑定</h3>
        <!-- 完整写法：v-on:click -->
        <button v-on:click="buyPS5(1)" class="btn btn-success">买PS5</button>
        <!-- 省略写法：:href -->
        <button @click="buyPS5(0)" class="btn btn-danger">不买PS5</button>
    </div>
    <script>
        Vue.createApp({/* options */
            data() {
                return {
                    komavideo: 'http://komavideo.com'
                }
            },
            methods: {
                buyPS5(val) {
                    val == 1 ? alert("买买买！！！") : alert("不买不买不买！！！")
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
