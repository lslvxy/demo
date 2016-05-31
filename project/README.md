以usermanage系统为例说明开发环境的搭建

首先运行本地子系统,注意Server.xml中path路径需要修改为`/`,启动后项目地址为:`localhost:8080/

本地svn检出 `staticresource` 文件夹,例如地址为`E:\WorkSpace\vsupa\staticresource`

下载nginx,地址为: `http://nginx.org/download/nginx-1.10.0.zip`,解压到本地,例如`d:/nginx`

修改'd:/nginx/nginx.conf'文件中server内容

server {
        listen       80;
        server_name  localhost;

        #charset koi8-r;

        #access_log  logs/host.access.log  main;


        location ^~/usermanage/ {
            proxy_pass http://127.0.0.1:8080/; //本地项目地址(注意最后的`/`不能少)
            proxy_set_header Host $http_host;
            proxy_set_header X-Real-IP $remote_addr;
            proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;


        }

        location ^~/dictionary/ {            //引用dictionary子系统需要配置
            proxy_pass http://192.168.1.127:8080/;
            proxy_set_header Host $http_host;
            proxy_set_header X-Real-IP $remote_addr;
            proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;

        }


        location / {
            root   E:/WorkSpace/vsupa/staticresource; //staticresource目录(注意目录是`/`,不是`\`)
            index  index.html;
        }
}

## 注:

测试阶段已部署的测试环境地址:

```
usermanage:http://120.25.148.72:8081/

dictionary: http://120.25.148.72:8071/

```

启动nginx.exe访问`http://localhost`即可

```
--staticresource  //项目根目录
    --js //js文件夹
        --systemname    //子系统名称
            --modulename  //模块名
    --css //css文件夹
        --systemname    //子系统名称
            --modulename  //模块名
    --images  //图片文件夹
        --systemname    //子系统名称
            --modulename  //模块名
    --views  //视图
        --systemname    //子系统名称
            --modulename  //模块名
                --index.html  //每个模块都要有index.html文件
    --libs           //库文件
    --index.html //模块首页
    --seajs.build.js
    --404.html
    --....

```
注意事项:

模块页面上不需要引用`seajs.build.js`以及`common.css`,只需要引入自己模块的css和js

引用地址统一使用绝对地址,例如`<script src="/js/dictionary/dict/index.js"></script>`,不要使用`../../`引入

ajax中url以等url同样使用绝对路径,例如`url:GLOBAL_VARS.usermanage+'user/login'`,`GLOBAL_VARS`是一个全局变量,不要使用`../`

页面跳转不要直接`window.location.href=''`,通过`UI.open(options)`方法加载

`UI.open('usermanage/personalsetting')`;// 跳转到已有模块,已有模块是指在functions表中配置的模块

//打开自定义页面,path填写地址栏显示的路径,一般为子系统名/模块名
// url为打开页面的地址
```
UI.open({
    path:'usermanage/info',
    url:'views/usermanage/user/info.html'
});
```
通过次方法打开的页面可以通过浏览器的后退和前进按钮返回到之前和之后的页面