### 提示弹框 

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

