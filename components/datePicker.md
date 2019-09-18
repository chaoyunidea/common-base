
## 时间选择 {docsify-ignore-all}

**标签名:fe-date-picker**

**说明:用于创建可由返回键控制的弹窗**

用于限制时间选择范围，在element ui <el-date-picker>;组件上增强了一个属性：choose-range,默认值是12（表示时间范围为12个月），如果type为daterange会自动限制可选时间范围。除此以外可以之间当<el-date-picker>用，预置了一下属性，可主动覆盖：
```
  {
    'type':'daterange',
    'editable':false,
    'unlink-pannels':true,
    'range-separator':'至',
    'start-placeholder':'开始日期',
    'end-placeholder':'结束日期',
    size:'small',
    value-format:'yyyy-mm-dd'
  }
```
增强了一个属性：value-fix,用于自定义字段如果只不是日期格式可以自动修复为空

 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| choose-range | 时间范围 | Number | 12  |
| type | 时间选择类型 | sting |    |
| value-fix | 自定义字段如果只不是日期格式可以自动修复为 | string | '' |


## 自定义时间选择 {docsify-ignore-all}

**标签名:fe-date-wraper**

**说明:用于自定义内容替换日期的输入框，中间出入插槽。**

```
  <fe-date-wraper><span> 时间选择</span> </fe-date-wraper>
```

