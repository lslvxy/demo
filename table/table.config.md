
表格的参数定义在 `jQuery.fn.bootstrapTable.defaults`。

|名称|类型|默认|说明|
|--|--|--|--|
|classes        |String   |table table-hover  |表格的类名称。默认情况下，表格是有边框的，你可以添加 'table-no-bordered' 来删除表格的边框样式。|
|height         |Number   |undefined          |定义表格的高度。|
|undefinedText  |String   |'-'                |定义undefined 内容|
|sortName       |String   |undefined          |排序字段，默认为空|
|sortOrder      |String   |'asc'              |正序或者倒序，只能为 'asc' 或者 'desc'.|
|columns        |Array    |[]                 |列配置，参照列参数章节|
|data           |Array    |[]                 |本地加载数据.|
|ajax           |Function |undefined          |ajax方法，不需要修改|
|method         |String   |'get'              |ajax提交方式，默认为get|
|url            |String   |undefined          |远程加载地址|
|cache          |Boolean  |false              |是否使用AJAX 缓存|
|contentType    |String   |'application/json' |The contentType of request remote data.|
|dataType       |String   |'json'             |The type of data that you are expecting back from the server.|
|queryParams    |Function |function(params)<br>{return params;}|远程请求参数，If queryParamsType = 'limit', 参数包括:limit, offset, search, sort, order<br>Else, 参数包括: pageSize, pageNumber, searchText, sortName, sortOrder. <br>Return false 终止请求  |
|queryParamsType|String   |'limit'            |默认 'limit'无需修改|
|responseHandler|Function|function(res) {<br>return res;<br>}  |响应格式化函数，一般不需要修改|
|pagination     |Boolean  |false              |是否分页|
|sidePagination |String   |'client'           |前端分页或者后端分页，只能为 'client' or 'server'.|
|pageNumber     |Number   |1                  |默认加载第一页|
|pageSize       |Number   |10                 |每页显示10条|
|pageList       |Array    |[10, 25, 50, 100, All]  |pagesize可选值列表，all表示全部 |
|showHeader     |Boolean  |true               |显示表格Header |
|showFooter     |Boolean  |true               |显示表格Footer |
|showColumns    |Boolean  |false              |显示可选列组件 |
|showRefresh    |Boolean  |false              |显示刷新按钮 |
|showPaginationSwitch     |Boolean  |false    |显示页码切换按钮 |
|minimumCountColumns      |Number   |1        |最少显示多少列  |
|detailFormatter|Function |function(index, row) {<br>return '';<br>}|格式化详细页面模式的视图。|
|toolbar        |String  |undefined|通过Jquery选择器设置工具栏，示例:<br>  #toolbar, .toolbar.  |
|checkboxHeader |Boolean  |true     |显示选择全部复选框|
|sortable       |Boolean |true     |排序|
