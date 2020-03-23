更多使用说明参见：<a href='https://github.com/thin-js/thin.js/wiki'>https://github.com/thin-js/thin.js/wiki<a>

## 开始使用

添加对jquery的引用,thinjs.com上的版本为3.4.1。
``` html
<script src="http://thinjs.com/jquery.js"></script>
```
添加对 thin.js的引用。
```html
<script src="http://thinjs.com/thin.min.js"></script>
``` 
如果你用到render以外的其他功能，还需要添加对thin.css的引用。(可选）
```html
<link rel="stylesheet" href="http://thinjs.com/thin.css">
```

使用渲染器
``` javascript
//var template={};
//var template=[];
$(selector).render({
        data:data,
        template:template
});
```
使用弹出层
``` javascript
poplayer({
    width: '500px', height: '500px', header: "a pop layer",
    template: [
        {
            e: "div", a: {id: "", name: "",  class: "pop-container",},
            t: [
                {e: "label", t: "sample", style: {}},
            ]
        },
        {e: "sapn", t: "say some thing"},
        {
            e: 'footer',
            t: [
                {
                    e: "button", a: {class: " ", type: "button"}, t: "确定",
                    click: function (ele) {
                      
                    }
                },
                {
                    e: "button", a: {class: "s_close", type: "button"}, t: "取消",
                    click: function (p) {
                        $(p.sender).closest("popmask").remove();
                    }
                }
            ]
        }
    ]

});
```
使用if 
``` javascript
var template={e: "sapn", t: {if: 1==1,then:"this is then",esle:"this is else"}};
```
使用switch
``` javascript
<select id="select1" name="select1">
        <option value="">option</option>
        <option value="A">optionA</option>
        <option value="A">optionB</option>
</select>
var template={e: "sapn", t: {switch: $("#select1").val(),
                                case:{"A":"case A","B":"case B"},
                                default:"switch default"
                             }
              };
```

## What's new ?

V1.1
* if
* switch case
* bind

for more help see /samples


