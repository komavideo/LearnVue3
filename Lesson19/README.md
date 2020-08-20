v-for渲染
==========

## Vue更新进度随时跟踪

https://github.com/vuejs/vue-next/releases

## 知识点

* 使用v-for的几个渲染方式

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h3>v-for普通用法</h3>
        <ul>
            <li v-for="item in languages">{{item.name}}</li>
        </ul>
        <hr>
        <h3>v-for索引</h3>
        <ul>
            <li v-for="(item, index) in languages">{{index+1}} - {{item.name}}</li>
        </ul>
        <hr>
        <h3>v-for循环对象</h3>
        <ul>
            <li v-for="val in game_sfv">{{val}}</li>
        </ul>
        <hr>
        <h3>v-for循环对象(附带标题)</h3>
        <ul>
            <li v-for="(val, title) in game_sfv">{{title}} -> {{val}}</li>
        </ul>
        <hr>
        <h3>v-for循环对象(附带标题+索引)</h3>
        <ul>
            <li v-for="(val, title, index) in game_sfv">{{index+1}} - {{title}} -> {{val}}</li>
        </ul>
    </div>
    <script>
        Vue.createApp({
            /* options */
            data() {
                return {
                    languages: [
                        {name: "Python"},
                        {name: "Java"},
                        {name: "Go"}
                    ],
                    game_sfv: {
                        name: "Street Fighter 5",
                        platform: "PS4",
                        developer: "Capcom",
                        release: "2016/02/16",
                        genre: "格斗"
                    }
                }
            },
            methods: {}
        }).mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
