
# 方法
---

## `$(selector).datetimepicker(options)`

初始化日期时间选择器。
## remove

参数: None

移除日期时间选择器。同时移除已经绑定的event、内部绑定的对象和HTML元素。

    $('#datetimepicker').datetimepicker('remove');

## show

参数: None

显示日期时间选择器。

    $('#datetimepicker').datetimepicker('show');

## hide

参数: None

隐藏日期时间选择器。

    $('#datetimepicker').datetimepicker('hide');

## update

参数: None

使用当前输入框中的值更新日期时间选择器。

    $('#datetimepicker').datetimepicker('update');

## setStartDate

参数:

    startDate (String)

给日期时间选择器设置一个新的起始日期。

    $('#datetimepicker').datetimepicker('setStartDate', '2012-01-01');

Omit startDate (or provide an otherwise falsey value) to unset the limit.

    $('#datetimepicker').datetimepicker('setStartDate');
    $('#datetimepicker').datetimepicker('setStartDate', null);

## setEndDate

参数:

    endDate (String)

给日期时间选择器设置结束日期。

    $('#datetimepicker').datetimepicker('setEndDate', '2012-01-01');

Omit endDate (or provide an otherwise falsey value) to unset the limit.

    $('#datetimepicker').datetimepicker('setEndDate');
    $('#datetimepicker').datetimepicker('setEndDate', null);

## setDaysOfWeekDisabled

参数:

    daysOfWeekDisabled (String|Array)

Sets the days of week that should be disabled.

    $('#datetimepicker').datetimepicker('setDaysOfWeekDisabled', [0,6]);

Omit daysOfWeekDisabled (or provide an otherwise falsey value) to unset the disabled days.

    $('#datetimepicker').datetimepicker('setDaysOfWeekDisabled');
    $('#datetimepicker').datetimepicker('setDaysOfWeekDisabled', null);
