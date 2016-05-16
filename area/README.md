```
<div id="area"></div>  

seajs.use('area',function(){
	$('#area').region();//默认样式

	$('#area').region({
		fields:["江苏省","无锡市","滨湖区"] //设置默认值
	});

	$('#area').region({
		fields:["江苏省","",""] //设置默认值,默认只选择省
	});

	$('#area').region({
		accuracy:1 //只能选择省,accuracy值可选1,2,3
	});
	
	//获取值
	var data=$('#area').data('region');
	//返回值为数组

});
```