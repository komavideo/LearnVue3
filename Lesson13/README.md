计算属性(getter)
===============

## 知识点

* Vue 3中的计算属性之getter

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <h3>我今年通关了这几个游戏：</h3>
        <ol>
            <li v-for="game in games">{{ game }}</li>
        </ol>
        <hr>
        <div class="lead">
            数数看，我今年一共通关了 <b class="text-danger">{{playedGameCount}}</b> 款游戏。
        </div>
    </div>
    <script>
        Vue.createApp({/* options */
            data() {
                return {
                    games: [
                        "纸片马里奥",
                        "勇者斗恶龙建造者2",
                        "赛博朋克2077",
                    ]
                }
            },
            computed: {
                playedGameCount() {
                    return this.games.length
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
