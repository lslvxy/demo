### alisa `Object`

别名配置，配置之后可在模块中使用require调用 `require('jquery')`;

```
seajs.config({
    alias: { 'jquery': 'jquery/jquery/1.10.1/jquery' }
});
```

```
define(function(require, exports, module) {
    //引用jQuery模块
    var $ = require('jquery');
});
```
### paths `Object`

设置路径，方便跨目录调用。通过灵活的设置`path`可以在不影响`base`的情况下指定到某个目录。

```
seajs.config({
    //设置路径
    paths: {
        'gallery': 'https://a.alipayobjects.com/gallery'
    },

    // 设置别名，方便调用
    alias: {
        'underscore': 'gallery/underscore'
    }
});
```

```
define(function(require, exports, module) {
    var _ = require('underscore');
     //=> 加载的是 https://a.alipayobjects.com/gallery/underscore.js
});
```

### vars `Object`

变量配置。有些场景下，模块路径在运行时才能确定，这时可以使用 `vars` 变量来配置。

`vars` 配置的是模块标识中的变量值，在模块标识中用 `{key}` 来表示变量。

```
seajs.config({
    // 变量配置
    vars: {
        'locale': 'zh-cn'
    }
})
```

```
define(function(require, exports, module) {
  var lang = require('./i18n/{locale}.js');
     //=> 加载的是 path/to/i18n/zh-cn.js
});
```

### map `Array`

该配置可对模块路径进行映射修改，可用于路径转换、在线调试等。

```
seajs.config({
    map: [
        [ '.js', '-debug.js' ]
    ]
});
```

```
define(function(require, exports, module) {
    var a = require('./a');
    //=> 加载的是 path/to/a-debug.js
});
```
