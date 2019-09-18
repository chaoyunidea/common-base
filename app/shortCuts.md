##  获取指定时间数组 {docsify-ignore}
**用于快速生成获取element ui 日期组件的picker-options里的shortcuts快捷日期数组**
*  API
  * ` $xgj.dateShortcuts(options) `
  

options参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| option | 内置关键字：不限，今天，昨天，本周，本月，下月... | 数组 |  |

* 示例：
  
```
   $xgj.dateShortcuts(['今天','昨天','本周','本月','下月'])

```
##  获取指定时间(按天)
*  API
  * ` $xgj.dateShortcuts.dayDiff(±n,reg) `

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| n | 以当天为准，前后天数 | number | |
| reg | 返回日期格式 |  String  |  |

* 示例：
  
```
   $xgj.dateShortcuts.dayDiff(6,'yyyy-MM-dd')//六天后
   $xgj.dateShortcuts.dayDiff(-6,'yyyy-MM-dd')//六天前
```

##  获取指定时间(按周)
*  API
  * ` $xgj.dateShortcuts.weekDiff(±n,reg) `

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| n | 以当天为准，前后周数 | number | |
| reg | 返回日期格式 |  String  |  |

* 示例：
  
```
   $xgj.dateShortcuts.weekDiff(6,'yyyy-MM-dd')//六周后
   $xgj.dateShortcuts.weekDiff(-6,'yyyy-MM-dd')//六周前
```

##  获取指定时间(按月)
*  API
  * ` $xgj.dateShortcuts.monthDiff(±n,reg) `

参数说明:

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| n | 以当天为准，前后月数 | number | |
| reg | 返回日期格式 |  String  |  |

* 示例：
  
```
   $xgj.dateShortcuts.monthDiff(6,'yyyy-MM-dd')//六月后
   $xgj.dateShortcuts.monthDiff(-6,'yyyy-MM-dd')//六月前
```