

### 基础表格
```
<table id="table"></table>
<div id="toolbar">
			<span class="btn btn-default">新增</span>
	<input type="text" class=text/>
		</div>


$('#table').bootstrapTable({
    url: 'http://mikepenz.com/jsfiddle/',
    pagination: true,
    sidePagination: 'server',
    queryParams: function(params) {
        return {
            accountPeriod: '2016-03',
            customerId: ''
        };
    },
    checkbox: true,
    showColumns: false,
    filterControl: true,
    showHeader: true,
	  toolbar:'#toolbar',
    columns: [{
        checkbox: true
    },
    {
        field: 'id',
        title: '编号',
        width: 200
    },
    {
        field: 'name',
        title: '名称',
        width: 200
    },
    {
        field: 'price',
        title: '价格',
        width: 200
    },
    {
        title: '操作',
        width: 200,
        formatter: function operateFormatter(value, row, index) {
            return ['<a class="like" href="javascript:void(0)" title="Like">',
            '关注',
            '</a>  ',
            '<a class="remove" href="javascript:void(0)" title="Remove">',
            '删除',
            '</a>'].join('');
        },
        events: {
            'click .like': function(e, value, row, index) {
                alert('You click like action, row: ' + JSON.stringify(row));
            },
            'click .remove': function(e, value, row, index) {
                $('#table').bootstrapTable('remove', {
                    field: 'id',
                    values: [row.id]
                });
            }
        }
    }]
});


```
 [在线demo](http://runjs.cn/code/dyhgfmzg)
