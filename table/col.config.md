列参数定义在： `jQuery.fn.bootstrapTable.columnDefaults`.

|名称|类型|默认|说明|
|--|--|--|--|
|radio        |Boolean    |false      |True 显示一个固定宽度的单选框|
|checkbox     |Boolean    |false      |True 现实一个固定宽度的复选框|
|field        |String     |undefined  |列对应的字段映射名称|
|title        |String     |undefined  |标题|
|titleTooltip |String     |undefined  |标题 tooltip 内容|
|class        |String     |undefined  |附加class|
|rowspan      |Number     |undefined  |rowspan|
|colspan      |Number     |undefined  |colspan|
|width        |Number {px or %}       |undefined|列宽度，通过`%`设置相对宽度，`px`设置绝对数据|
|sortable     |Boolean    |false      |排序  |
|order        |String     |'asc'      |排序方式 can only be 'asc' or 'desc'.|
|visible      |Boolean    |true       |False 隐藏该列|
|formatter    |Function   |undefined  |数据格式化函数function(value,row,index)|
|events       |Object     |undefined  |事件，function(event,value,row,index)  |
