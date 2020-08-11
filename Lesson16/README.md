观察者属性
==========

## 知识点

* 使用观察者属性(watch)侦测数据的更改

## 实战演习

~~~html
<body>
    <div id="hello-vue" class="m-3 p-3 border border-success">
        <p>
            有什么问题吗:
            <input v-model="question" />
        </p>
        <p>
            {{ msg }}
            <hr>
            <img :src="answer" alt="">
        </p>
    </div>
    <script>
        Vue.createApp({
            /* options */
            data() {
                return {
                    question: '',
                    answer: '',
                    msg: "",
                }
            },
            watch: {
                question(newQuestion, oldQuestion) {
                    if (newQuestion.indexOf('?') > -1) {
                        this.getAnswer()
                    } else {
                        this.msg = ""
                        this.answer = ""
                    }
                }
            },
            methods: {
                getAnswer() {
                    this.msg = "考虑中..."
                    axios
                        .get('https://yesno.wtf/api')
                        .then(response => {
                            this.msg = response.data.answer
                            this.answer = response.data.image
                        })
                        .catch(error => {
                            this.msg = 'Error! Could not reach the API. ' + error
                        })
                }
            }
        }).mount('#hello-vue')
    </script>
    <script src="https://cdn.jsdelivr.net/npm/axios@0.12.0/dist/axios.min.js"></script>
</body>
~~~

## 课程文件

https://github.com/komavideo/LearnVue3

## 小马视频频道

http://komavideo.com
