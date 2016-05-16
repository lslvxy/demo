# Methods

---

调用方法: `$('#table').bootstrapTable('method', parameter);`.


|名称|参数|说明|示例|
|--|--|--|--|
|getOptions|none|返回配置项|[getOptions](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/getOptions.html)|
|getSelections|none|返回选择的内容|[getSelections](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/getSelections.html)|
|getAllSelections|none|返回选择全部的内容.|[getAllSelections](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/getAllSelections.html)|
|getData|useCurrentPage|返回当前页的数据.|[getData](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/getData.html)|
|getRow|index|通过index查询一行数据||
|getRowByUniqueId|id|通过id查询一行数据|[getRowByUniqueId](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/getRowByUniqueId.html)|
|load|data|load 数据|[load](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/load.html)|
|remove|params|删除一行数据|[remove](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/remove.html)|
|removeAll|-|删除所有数据|[removeAll](http://issues.wenzhixin.net.cn/bootstrap-table/#methods/removeAll.html)|
|insertRow|params|新增一行||
|updateRow|params|更新一行数据, the param contains following properties: <br>  index: the row index to be updated. <br>row: the new row data.  ||
|showRow|params|显示一行数据. The param must contain at least one of the following properties:  index: the row index.  uniqueId: the value of the uniqueId for that row.||
|hideRow|params|隐藏一行数据. The param must contain at least one of the following properties:  index: the row index.  uniqueId: the value of the uniqueId for that row.||
|getRowsHidden|boolean|获取隐藏的行||
|refresh|params|刷新表格数据 set <code>{query: {foo: 'bar'}}</code>||
|checkAll|none|选择全部||
|uncheckAll|none|取消选择全部||
|check|index|选择一行，index从0开始||
|uncheck|index|取消选择||
|showColumn|field|显示列||
|hideColumn|field|隐藏列.||
|getHiddenColumns|-|获取隐藏的列.||
