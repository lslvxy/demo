* change  值变更时触发

* select2:open  下拉框打开之后触发

* select2:opening 下拉框打开之前触发(可以被阻止)

* select2:close 下拉框关闭之后触发

* select2:closing 下拉框关闭之前触发(可以被阻止)

* select2:select 值被选择时触发

* select2:selecting 值被选择前触发(可以被阻止)

* select2:unselect 值被取消选择时触发

* select2:unselecting 值被取消选择前触发(可以被阻止)


```
$('select').val('US'); // Select the option with a value of 'US'
$('select').trigger('change'); // Notify any JS components that the value changed

```