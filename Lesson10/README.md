Vue实例的生命周期
===============

## 知识点

每个Vue实例在创建时都会经历一系列初始化步骤-例如，它需要设置数据观察，
编译模板，将实例安装到DOM以及在数据更改时更新DOM。在此过程中，它还要
运行称为生命周期的钩子函数，使用户有机会在特定阶段添加自己的代码。

## 官网生命周期API

https://v3.vuejs.org/api/options-lifecycle-hooks.html

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        {{ x + y }}
    </div>
    <script>
        Vue.createApp({/* options */
            data() {
                return {
                    x: 10,
                    y: 20,
                }
            },
            created() {
                // 组件生成时
                console.log('x + y is: ' + (this.x + this.y))
            }
        }).mount('#hello-vue')
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
