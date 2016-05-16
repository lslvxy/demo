* `ajax.processResults`函数用来格式化远程数据格式

```
$('select').select2({
  ajax: {
    url: '/example/api',
    processResults: function (data) {
      return {
        results: data.items
      };
    }
  }
});

```

* 附加请求参数

```
$('select').select2({
  ajax: {
    data: function (params) {
      var query = {
        search: params.term,
        page: params.page
      }
      // Query paramters will be ?search=[term]&page=[page]
      //term和page是默认参数名,可以通过此方法修改为search和page
      return query;
    }
  }
});

```



