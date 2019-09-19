## 表头筛选 {docsify-ignore-all}
 
**标签名：fe-filter-select**

```
 <template>
    <fe-filter-select :filterData="" @filterStatus.sync="" multi="" prop=""> </fe-filter-select>
 </template>

     
```


 
## 标签属性说明

| 属性 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| prop | 该筛选对应的filterData的key | String |  |
| filterData | 过滤的选择项 | object |  0  |
| multi | 是否多选 | Bool | true |   
| filterStatus | 筛选配置的结果 | object |  |

## 事件说明

| 事件名 | 说明 | 类型 | 默认值 |
| --- | --- | --- | --- |
| change | 确定筛选时触发 | Function |    |

 


 
