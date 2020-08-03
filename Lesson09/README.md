Vue对象实例
==========

## 知识点

* 了解Vue对象实例的生成与使用

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        {{ a }}
    </div>
    <script>
        // 定义自己的数据对象
        const myData = { a: 10 }
        const vm = Vue.createApp({/* options */
            data() {
                // App返回自定义的数据对象
                return myData
            }
        }).mount('#hello-vue')
        // 打印数据
        console.log(vm.a)
        console.log(vm.$data)
        console.log(myData)
        // 改变数据的值
        vm.a = 100
        console.log(vm.a)
        console.log(vm.$data) // Vue实例属性
        console.log(myData)
    </script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
