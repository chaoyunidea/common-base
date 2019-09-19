## 颜色选择

**$xgj.echarts.COLOR[index]**   

 
* 参数:：
  * ``{Number}  index ``  



* 返回值：``{String} valaue``


* 用法：

  从预设的色组里选取对应的色值，具体色值查看公共库代码
  

* 示例：

```
  var color = $xgj.echarts.COLOR[0];

```
 
***



## 混合echarts配置对象 

**$xgj.echarts.mixin(optionOrigin,extend)**  

* 参数:：
  * ``{ Object}  optionOrigin ``
  * ``{ Object}  extend ``

* 返回值：
  * ``{Object} options``
 
* 示例：
```
  $xgj.echarts.mixin(optionOrigin,extend)
```


 

*** 


 
 ##  构造echarts的配置项的对象 

**$xgj.echarts.createFactory(option)**


* 参数:：
  * ``{ Object}  option ``

 

* 返回值：
    * ``{Class} factory``
 
* 示例：

```
  $xgj.echarts.createFactory(option) 
``````