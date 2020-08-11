条件渲染
========

## 知识点

* 根据条件渲染页面内容(v-if/v-else-if/v-else)

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <div v-if="isLoveGame" class="display-5 text-primary">一定要买 PS5.</div>
        <div v-else class="display-5 text-success">好好学习，天天向上。</div>
        <hr>
        <template v-if="isLoveGame">
            <h3>必买游戏</h3>
            <ol>
                <li>塞伯朋克2077</li>
                <li>文明7</li>
                <li>街头霸王6</li>
            </ol>
        </template>
        <hr>
        <div v-if="this.playedYears >= 10" class="display-5">资深玩家</div>
        <div v-else-if="this.playedYears >= 5" class="display-5">老玩家</div>
        <div v-else-if="this.playedYears >= 2" class="display-5">入门级</div>
        <div v-else class="display-5">菜鸟一枚</div>
    </div>
    <script>
        Vue.createApp({
            /* options */
            data() {
                return {
                    isLoveGame: true,
                    playedYears: 10,
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
