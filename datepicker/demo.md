#示例
---
## Default
    <input size="16" type="text" value="2012-06-15 14:45" readonly class="form_datetime">

    <script type="text/javascript">
        $(".form_datetime").datetimepicker({format: 'yyyy-mm-dd hh:ii'});
    </script>   


##  position
    <div class="input-append date form_datetime">
        <input size="16" type="text" value="" readonly>
        <span class="add-on"><i class="icon-th"></i></span>
    </div>

    <script type="text/javascript">
        $(".form_datetime").datetimepicker({
            format: "dd MM yyyy - hh:ii"
        });
    </script>            


## Advanced

    <div class="input-append date form_datetime" data-date="2013-02-21T15:25:00Z">
        <input size="16" type="text" value="" readonly>
        <span class="add-on"><i class="icon-remove"></i></span>
        <span class="add-on"><i class="icon-calendar"></i></span>
    </div>

    <script type="text/javascript">
        $(".form_datetime").datetimepicker({
            format: "dd MM yyyy - hh:ii",
            autoclose: true,
            todayBtn: true,
            startDate: "2013-02-14 10:00",
            minuteStep: 10
        });
    </script>            
