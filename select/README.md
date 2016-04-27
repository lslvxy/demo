官方网站: [http://select2.github.io/](http://select2.github.io/)

select2组件已经集成到seajs中,不需要单独引用js和css文件

## 基本使用

```
<script type="text/javascript">
  $('select').select2();
</script>
```

## 单选/分组
```
<select class="js-example-basic-single">
  <optgroup label="Alaskan/Hawaiian Time Zone">
    <option value="AK">Alaska</option>
    <option value="HI">Hawaii</option>
  </optgroup>
  <optgroup label="Pacific Time Zone">
    <option value="CA">California</option>
    <option value="NV">Nevada</option>
    <option value="OR">Oregon</option>
    <option value="WA">Washington</option>
  </optgroup>
  <optgroup label="Mountain Time Zone">
    <option value="AZ">Arizona</option>
    <option value="CO">Colorado</option>
    <option value="ID">Idaho</option>
    <option value="MT">Montana</option>
    <option value="NE">Nebraska</option>
  </optgroup>
</select>

<script type="text/javascript">
$(document).ready(function() {
  $(".js-example-basic-single").select2();
});
</script>
```

## 多选

添加`multiple`属性

```
<script type="text/javascript">
$(".js-example-basic-multiple").select2();
</script>

<select class="js-example-basic-multiple" multiple="multiple">
  <option value="AL">Alabama</option>
    ...
  <option value="WY">Wyoming</option>
</select>

```

## Placeholders

```
$(".js-example-placeholder-single").select2({
  placeholder: "Select a state",
  allowClear: true
});
 
$(".js-example-placeholder-multiple").select2({
  placeholder: "Select a state"
});
```

## 通过数组加载数据

```
<script type="text/javascript">
var data = [{ id: 0, text: 'enhancement' }, { id: 1, text: 'bug' }, { id: 2, text: 'duplicate' }, { id: 3, text: 'invalid' }, { id: 4, text: 'wontfix' }];

$(".js-example-data-array").select2({
  data: data
})

$(".js-example-data-array-selected").select2({
  data: data
})
</script>

<select class="js-example-data-array"></select>

<select class="js-example-data-array-selected">
  <option value="2" selected="selected">duplicate</option>
</select>
```

## 通过远程加载数据

```
<select class="js-data-example-ajax">
  <option value="3620194" selected="selected">select2/select2</option>
</select>
```

通过`ajax配置`来进行远程数据的加载,具体配置项请参考[OPTIONS](./options.md)

```
$(".js-data-example-ajax").select2({
  ajax: {
    url: "https://api.github.com/search/repositories",
    dataType: 'json',
    delay: 250,
    data: function (params) {
      return {
        q: params.term, // search term
        page: params.page
      };
    },
    processResults: function (data, params) {
      // parse the results into the format expected by Select2
      // since we are using custom formatting functions we do not need to
      // alter the remote JSON data, except to indicate that infinite
      // scrolling can be used
      params.page = params.page || 1;

      return {
        results: data.items,
        pagination: {
          more: (params.page * 30) < data.total_count
        }
      };
    },
    cache: true
  },
  escapeMarkup: function (markup) { return markup; }, // let our custom formatter work
  minimumInputLength: 1,
  templateResult: formatRepo, // omitted for brevity, see the source of this page
  templateSelection: formatRepoSelection // omitted for brevity, see the source of this page
});
```


## Disabled 状态

直接给`<select>`标签加上`disabled`的属性或者通过配置项`disabled: true`来实现


## Disabled单条记录

```
<select class="js-example-disabled-results">
  <option value="one">First</option>
  <option value="two" disabled="disabled">Second (disabled)</option>
  <option value="three">Third</option>
</select>
```

## 多选数量限制

在基本的多选下拉框基础上加上配置项`maximumSelectionLength`表示最多能选多少项

```
$(".js-example-basic-multiple-limit").select2({
  maximumSelectionLength: 2
});
```

## 隐藏 search box

```
$(".js-example-basic-hide-search").select2({
  minimumResultsForSearch: Infinity
});

```