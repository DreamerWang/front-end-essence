# Web前端精髓

```js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>
    <div id="app">
        <parent></parent>
    </div>
    <template id="ban">
        <!--模板可以直接在上面定义然后直接用id引入  -->
        <div>
            <div>parentwu</div>
            <!-- 传递数据 -->
            <child :str="msg"></child>
        </div>
    </template>
    <script type="text/javascript" src="./vue2.js"></script>
    <script type="text/javascript">
        var vm = new Vue({
            el: "#app",
            data: {
            },
            components: {
                parent: {
                    template: "#ban",
                    data() {
                        return {
                            msg: "xianqiang"
                        }
                    },
                    components: {
                        child: {
                            template: "<div>child{{str}}</div>",
                            // 接收数据
                            props:['str']
                        }             
                    }
                }
            }
        })
    </script>
</body>
</html>
```

> 支持作者请点击右上角的Star按钮
