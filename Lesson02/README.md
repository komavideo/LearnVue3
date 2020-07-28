Vue 3的安装
==========

## Vue更新进度随时跟踪

https://github.com/vuejs/vue-next/releases

## 知识点

* HTML中引用(CDN或本地)
* 命令行工具安装(NPM, YARN)

## 官网

https://v3.vuejs.org/guide/installation.html

## 实战演习

### HTML引用的方式

~~~html
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vue 3.0 - 小马技术</title>
    <script src="https://unpkg.com/vue@next"></script>
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/5.0.0-alpha1/css/bootstrap.min.css" integrity="sha384-r4NyP46KrjDleawBgD5tp8Y7UzmLA05oM1iAEQ17CSuDqnUK2+k9luXQOfXJCJ4I" crossorigin="anonymous"> 
</head>
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        {{ message }}
    </div>
    <script>
        const HelloVueApp = {
            data() {
                return {
                    message: 'Hello Vue!!'
                }
            }
        }
        Vue.createApp(HelloVueApp).mount('#hello-vue')
    </script>    
</body>
</html>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
