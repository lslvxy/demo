
<table class="table">
    <thead>
    <tr>
        <th>Option 事件</th>
        <th>jQuery 事件</th>
        <th>参数</th>
        <th>描述</th>
    </tr>
    </thead>
    <tbody>
    <tr>
        <td>onAll</td>
        <td>all.bs.table</td>
        <td>name, args</td>
        <td>
        所有的事件都会触发该事件，参数包括：<br>
        name：事件名，<br>
        args：事件的参数。
        </td>
    </tr>
    <tr>
        <td>onClickRow</td>
        <td>click-row.bs.table</td>
        <td>row, $element</td>
        <td>
        当用户点击某一行的时候触发，参数包括：<br>
        row：点击行的数据，<br>
        $element：tr 元素。
        </td>
    </tr>
    <tr>
        <td>onDblClickRow</td>
        <td>dbl-click-row.bs.table</td>
        <td>row, $element</td>
        <td>
        当用户双击某一行的时候触发，参数包括：<br>
        row：点击行的数据，<br>
        $element：tr 元素。
        </td>
    </tr>
    <tr>
        <td>onClickCell</td>
        <td>click-cell.bs.table</td>
        <td>field, value, row, $element</td>
        <td>
        当用户点击某一列的时候触发，参数包括：<br>
        field：点击列的 field 名称，<br>
        value：点击列的 value 值，<br>
        row：点击列的整行数据，<br>
        $element：td 元素。
        </td>
    </tr>
    <tr>
        <td>onDblClickCell</td>
        <td>dbl-click-cell.bs.table</td>
        <td>field, value, row, $element</td>
        <td>
        当用户双击某一列的时候触发，参数包括：<br>
        field：点击列的 field 名称，<br>
        value：点击列的 value 值，<br>
        row：点击列的整行数据，<br>
        $element：td 元素。
        </td>
    </tr>
    <tr>
        <td>onSort</td>
        <td>sort.bs.table</td>
        <td>name, order</td>
        <td>
        列排序的时候触发，参数包括: <br>
        name: the sort column field name<br>
        order: the sort column order.
        </td>
    </tr>
    <tr>
        <td>onCheck</td>
        <td>check.bs.table</td>
        <td>row</td>
        <td>
      复选框选择的时候触发，参数包括: <br>
        row: the record corresponding to the clicked row.
        $element: the DOM element checked.
        </td>
    </tr>
    <tr>
        <td>onUncheck</td>
        <td>uncheck.bs.table</td>
        <td>row</td>
        <td>
      复选框取消选择的时候触发，参数包括: <br>
        row: the record corresponding to the clicked row.
        $element: the DOM element unchecked.
        </td>
    </tr>
    <tr>
        <td>onCheckAll</td>
        <td>check-all.bs.table</td>
        <td>rows</td>
        <td>
      全选的时候触发，参数包括: <br>
        rows: array of records corresponding to newly checked rows.
        </td>
    </tr>
    <tr>
        <td>onUncheckAll</td>
        <td>uncheck-all.bs.table</td>
        <td>rows</td>
        <td>
      取消全选的时候触发，参数包括: <br>
        rows: array of records corresponding to previously checked rows.
        </td>
    </tr>
    <tr>
        <td>onCheckSome</td>
        <td>check-some.bs.table</td>
        <td>rows</td>
        <td>
        选择部分的时候触发，参数包括: <br>
        rows: array of records corresponding to previously checked rows.
        </td>
    </tr>
    <tr>
        <td>onUncheckSome</td>
        <td>uncheck-some.bs.table</td>
        <td>rows</td>
        <td>
        取消选择部分的时候触发，参数包括: <br>
        rows: array of records corresponding to previously checked rows.
        </td>
    </tr>
    <tr>
        <td>onLoadSuccess</td>
        <td>load-success.bs.table</td>
        <td>data</td>
        <td>加载数据成功的时候触发
        </td>
    </tr>
    <tr>
        <td>onLoadError</td>
        <td>load-error.bs.table</td>
        <td>status</td>
        <td>加载数据失败的时候触发</td>
    </tr>
    <tr>
        <td>onPageChange</td>
        <td>page-change.bs.table</td>
        <td>number, size</td>
        <td>切换页码触发</td>
    </tr>
    <tr>
        <td>onPreBody</td>
        <td>pre-body.bs.table</td>
        <td>data</td>
        <td>渲染之前触发</td>
    </tr>
    <tr>
        <td>onPostBody</td>
        <td>post-body.bs.table</td>
        <td>none</td>
        <td>渲染完成之后触发</td>
    </tr>
    <tr>
       <td>onPostHeader</td>
       <td>post-header.bs.table</td>
       <td>none</td>
       <td>表格header 渲染之后触发</td>
    </tr>
    <tr>
        <td>onExpandRow</td>
        <td>expand-row.bs.table</td>
        <td>index, row, $detail</td>
        <td>当点击详细图标展开详细页面的时候触发。</td>
    </tr>
    <tr>
       <td>onCollapseRow</td>
       <td>collapse-row.bs.table</td>
       <td>index, row</td>
       <td>当点击详细图片收起详细页面的时候触发。</td>
    </tr>
    <tr>
       <td>onRefreshOptions</td>
       <td>refresh-options.bs.table</td>
       <td>options</td>
       <td>刷新的时候触发</td>
    </tr>
    </tbody>
</table>
