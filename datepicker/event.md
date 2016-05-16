#事件
---


Datetimepicker 类暴露了一组event用以对日期进行操作。
## show

当选择器显示时被触发。
## hide

当选择器隐藏时被触发。
## changeDate

当日期被改变时被触发。

    $('#date-end')
    .datetimepicker()
    .on('changeDate', function(ev){
        if (ev.date.valueOf() < date-start-display.valueOf()){
            ....
        }
    });


## changeYear

当十年视图上的年视图view被改变时触发。
## changeMonth

当年视图上的月视图view被改变时触发。
## outOfRange

当用户选择的日期超出startDate 或endDate 时，或者通过setDate 或 setUTCDate方法设置日期超出范围时被触发。
