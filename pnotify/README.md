推荐使用 UI (UI的封装主要是为了兼容以前的旧代码,以及统一调用格式,类似java中的接口)

```
UI.notify("message");  //默认提示success消息

UI.notify(options);  //配置项调用,同默认配置

```



PNotify默认调用方式

```
 new PNotify({
    title:'页面加载失败', //标题
    text:'请联系客服或者系统管理员解决',//提示内容
    type:'error'  //提示类型 ,'info','error',默认'success'
});
```