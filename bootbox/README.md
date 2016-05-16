### 提示弹框 


推荐使用 UI (UI的封装主要是为了兼容以前的旧代码,以及统一调用格式,类似java中的接口)

```
UI.alert('message');	//默认弹窗(等同`bootbox.alert(message) `)

UI.alert(options,callback);	//options:配置项,callback 回调函数

UI.confirm(options, callback, callbackNo); //options为String或者object,
										  //callback确定触发,callbackNo 取消触发

UI.dialog(options); //弹窗配置


```

```
UI.dialog({
        title: '新建窗口',  //标题
        message: 'xxxxx',   //内容(String | Element) 字符串或者页面元素
        buttons:[{			// 按钮组
            text: '确定',
            'class': 'btn-default',
            click: function() {
            }
        }, {
            text: '取消'
        }]
    });
```

* 默认 

`bootbox.alert(message) `

* 包含回调函数

`bootbox.alert("Your message here…", function(){ /* your callback code */ })`

* 配置项

```
bootbox.alert({ 
    size: 'small',
    message: "Your message here…", 
    callback: function(){ /* your callback code */ }
})
```

### 确认弹框

* 默认

 `bootbox.confirm("Your message here…", function(result){ /* your callback code */ })`

 * 配置项

 ```
bootbox.confirm({ 
    size: 'small',
    message: "Your message here…", 
    callback: function(result){ /* your callback code */ }
})
 ```

 ### 带一个输入框的弹窗

 * 默认

 `bootbox.prompt("Your message here…", function(result){ /* your callback code */ })`

 * 配置项

 ```
bootbox.prompt({ 
    size: 'small',
    message: "Your message here…", 
    callback: function(result){ /* your callback code */ }
})
 ```

 ### Dialog弹窗

* 调用方式

 `bootbox.dialog({options})`

* 配置项

|名称|类型|说明|
|--|--|--|
|message|String|弹窗标题|
|title|String|弹窗标题|
|callback|Function|回调函数|
|onEscape|Boolean/Function|ESC键设为false则不关闭弹窗|
|closeButton|Boolean|是否显示关闭按钮,默认true|
|animate|Boolean|动画,默认true|
|className|String|附加css|
|size|String|'large'或者'small'|
|buttons|Object|按钮组|

