样式单绑定
=========

## Vue更新进度随时跟踪

https://github.com/vuejs/vue-next/releases

## 知识点

* 在组件中绑定css样式单

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <div class="text-danger border display-5">我爱NBA!</div>
        <hr>
        <div :class="{ 'text-danger': isLoveCBA, border: isLoveCBA, 'display-5': isLoveCBA }">我爱CBA!</div>
        <button @click="this.isLoveCBA=!this.isLoveCBA" class="btn btn-info">爱CBA</button>
        <hr>
        <div :class="cssCUBA">我爱CUBA!</div>
        <button @click="this.cssCUBA=this.cssTitle" class="btn btn-info">爱CUBA</button>
        <hr>
        <!-- 直接绑定style属性, 不用class方式 -->
        <div :style="cssWNBA">我爱WNBA!</div>
    </div>
    <script>
        Vue.createApp({
            /* options */
            data() {
                return {
                    isLoveCBA: false,
                    cssCUBA: {},
                    cssTitle: {
                        'text-danger': true,
                        'border': true,
                        'display-5': true,
                    },
                    cssWNBA: {
                        color: 'red',
                        fontSize: '36px'
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
